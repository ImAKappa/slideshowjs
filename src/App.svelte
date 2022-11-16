<script lang="ts">
  import TitleSlide from './lib/TitleSlide.svelte';
  import Slide from './lib/Slide.svelte';

  let numSlides = 5;
  let slideIndices = [...Array(numSlides).keys()];
</script>

<main class="min-h-screen flex flex-col p-10 align-center justify-center">

  <!-- Slideshow -->
  <div class="overflow-x-scroll flex flex-row">
    <TitleSlide />

    <Slide slideNum={0} graphicPath="somehwere/over/there/"/>
    <Slide slideNum={1} graphicPath="somehwere/under/where/"/>
    {#each slideIndices as i}
      <Slide slideNum={i+2}/>
    {/each}
  </div>
</main>

<!-- <style>
  main {
    overflow-x: scroll;
    display: flex;
    flex-direction: row;
    margin: 0;
    padding: 2.2em;
  }
</style> -->