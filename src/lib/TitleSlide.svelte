<script lang="ts">
    import SlideFrame from "./SlideFrame.svelte";

    export let title: string = "Default Title";
    export let subtitle: string = null;
    export let graphicPath: string = "./title/graphic";
</script>

<SlideFrame>
    <h1>{title}</h1>
    {#if subtitle}
        <p>{subtitle}</p>
    {/if}
    {#if graphicPath}
        <p>{graphicPath}</p>
    {/if}
</SlideFrame>

<!-- <style>
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
</style> -->