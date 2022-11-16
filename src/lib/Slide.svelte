<script lang="ts">
    import IntersectionObserver from "svelte-intersection-observer";
    import Text from "./Text.svelte";

    export let title: string = "Default Title";
    export let graphicPath: string = null;
    export let slideNum: number;

    let text;
    let graphic;
</script>

<section>
    <!-- <p>Slide num: {slideNum}</p> -->
    <h2>{title}</h2>

    <div class="container">
        <div class="left-side">
            <Text>
                <p>{graphicPath}</p>
            </Text>
        </div>
        <div class="right-side">
            <Text>
                <p>Hello World!</p>
            </Text>
        </div>
    </div>
</section>

<style>
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
</style>