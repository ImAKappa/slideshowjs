<script lang="ts">
  import TitleSlide from './lib/TitleSlide.svelte';
  import Slide from './lib/Slide.svelte';

  import IntersectionObserver from "svelte-intersection-observer";

  let numSlides = 5;
  let slideIndices = [...Array(numSlides).keys()];
</script>

<main>
  <TitleSlide />

  <Slide slideNum={0} graphicPath="somehwere/over/there/"/>
  <Slide slideNum={1} graphicPath="somehwere/under/where/"/>

  <!-- {#each slideIndices as i}
    <Slide slideNum={i+1}/>
  {/each} -->
</main>

<style>
  main {
    overflow-x: scroll;
    display: flex;
    margin: 0;
  }
</style>