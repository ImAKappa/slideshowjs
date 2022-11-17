<script lang="ts">
    import SlideFrame from "./SlideFrame.svelte";
    import Fade from "./Fade.svelte";

    export let slideNum: number;
    export let title: string = "Default Title";
    export let svgPath: string = null;
    export let imagePath: string = null;
    export let videoPath: string = null;
    export let caption = null;
</script>

<SlideFrame>
    <!-- <p>Slide num: {slideNum}</p> -->
    <h2 class="text-4xl">{title}</h2>

    <div class="flex flex-col justify-around">
        {#if videoPath}
            <video controls width="250">
                <source src="{videoPath}" type="video/webm">
                <source src="{videoPath}" type="video/mp4">
            </video>
            <p>If video doesn't load, try <a class="text-blue-200 underline" href="{videoPath}" target="_blank">this link</a></p> 
        {/if}
        {#if svgPath}
            <p>SVG Here</p>
        {/if}
        {#if imagePath}
        <div class="mt-10">
            <img src="{imagePath}" alt="{imagePath}">
        </div>
        {/if}
        {#if caption}
        <div class="text-2xl m-10">
            <Fade>
                <p>{caption}</p>
            </Fade>
        </div> 
        {/if}
    </div>
</SlideFrame>

<!-- <style>
    section {
        min-width: 96%;
        min-height: 90%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-size: 4ch;
        margin: 0 0.5em;
        /* border: 1px solid var(--main-txt-color); */
        box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
        transition-duration: 0.4s;
        border-radius: 10px;
    }

    section:hover {
        box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.4), 0 2px 4px -2px rgb(0 0 0 / 0.4); 
    }

    h2 {
        margin: 0.5em;
        text-align: center;
    }

    .container {
        min-width: 90%;
        min-height: 80%;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        border: 2px solid purple;
    }

    .left-side {
        border: 2px solid green;
    }

    .right-side {
        border: 2px solid red;
    }
</style> -->