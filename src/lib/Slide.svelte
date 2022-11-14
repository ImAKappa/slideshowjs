<script lang="ts">
    import { onMount } from "svelte";


    export let title: string = "Default Title";
    export let body: string = null;
    export let graphicPath: string = null;
    export let slideNum: number;

    export let observer: IntersectionObserver;

    onMount(() => {
        let hidden = document.querySelector(`.appear-${slideNum}`);
        observer.observe(hidden);
    });
</script>

<section>
    <p>Slide num: {slideNum}</p>
    <h2>{title}</h2>
    {#if body}
        <p>{body}</p>
    {/if}
    {#if graphicPath}
        <p>{graphicPath}</p>
    {/if}
    <p class="hidden appear-{slideNum}">Hello</p>
</section>

<style>
    section {
        min-width: 80vw;
        min-height: 80vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-size: 4ch;
        border: 1px solid white;
    }

    h1 {
        margin: 0;
    }

    .hidden {
        opacity: 0;
        transition-duration: 3s;
    }
</style>