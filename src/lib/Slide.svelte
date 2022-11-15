<script lang="ts">
    import IntersectionObserver from "svelte-intersection-observer";
    import { fade } from "svelte/transition";

    export let title: string = "Default Title";
    export let body: string = null;
    export let graphicPath: string = null;
    export let slideNum: number;

    let node;
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

    <IntersectionObserver element={node} let:intersecting threshold={1.0}>
        <div bind:this={node}>
            <p style="opacity: {intersecting ? '1.0' : '0.0'}">Hello World!</p>
        </div>
    </IntersectionObserver>
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

    p {
        transition-duration: 3s;
    }
</style>