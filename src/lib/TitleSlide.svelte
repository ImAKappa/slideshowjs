<script lang="ts">
    import SlideFrame from "./SlideFrame.svelte";
    import Walking from "./Walking.svelte";

    export let title: string = "Default Title";
    export let subtitle: string = null;
    export let author: string = null;
</script>

<SlideFrame>
    <!-- <p>Slide num: {slideNum}</p> -->
    <h1 class="text-6xl">{title}</h1>
    <h3 class="text-2xl">{subtitle}</h3>

    <div class="flex flex-col justify-around">
        <div class="w-52">
            <Walking />
        </div>

        <div class="flex flex-col justify-around">
            <p>{author}</p>
        </div>
    </div>
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