<script lang="ts">
  import TitleSlide from './lib/TitleSlide.svelte';
  import Slide from './lib/Slide.svelte';

  let numSlides = 5;
  let slideIndices = [...Array(numSlides).keys()];
</script>

<main class="w-full mx-80 h-screen m-10 text-center overflow-hidden flex items-center">

  <!-- Slideshow Slider -->
    <!-- Slides -->
    <div class="flex overflow-x-auto snap-x snap-mandatory scroll-smooth h-full">
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