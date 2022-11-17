<script lang="ts">
  import Slide from './lib/Slide.svelte';
  import TitleSlide from './lib/TitleSlide.svelte';

  type SlideType = {
    slideNum: number
    title: string
    svgPath?: string,
    imagePath?: string
    videoPath?: string
    caption?: string
  }

  let slides: SlideType[] = [
    {slideNum: 0, title: "My Passion: Exploring", svgPath: "./svg/Man_walking_icon.svg", caption: "By Alex Kappen"},
    {slideNum: 1, title: "Getting Into Trouble", caption: "TL;DR: Accidentally trapped myself by a highway, jumped a fence, ripped my shirt, while carrying a slightly stale full pizza from Papa John's, to catch a bus to my friend's place"}
  ];
</script>

<main class="w-full mx-40 h-4/5 text-center overflow-hidden flex items-center drop-shadow-lg rounded-lg">

  <!-- Slideshow Slider -->
    <div class="flex overflow-x-auto snap-x snap-mandatory scroll-smooth h-full">
      <!-- Title Slide -->
      <TitleSlide title={"Exploring"} subtitle={"Passion Presentation"} author={"Alex Kappen, Nov 2022"}/>
      <!-- Slides -->
      {#each slides as slide (slide.slideNum)}
        <Slide {...slide}/>
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