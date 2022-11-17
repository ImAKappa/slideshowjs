<script lang="ts">
  import TitleSlide from './lib/TitleSlide.svelte';
  import Slide from './lib/Slide.svelte';

  let numSlides = 5;
  let slideIndices = [...Array(numSlides).keys()];
</script>

<main class="w-full mx-40 h-4/5 text-center overflow-hidden flex items-center drop-shadow-lg rounded-lg">

  <!-- Slideshow Slider -->
    <!-- Slides -->
    <div class="flex overflow-x-auto snap-x snap-mandatory scroll-smooth h-full">
      <!-- Title Slide -->
      <Slide slideNum={0} graphicPath={"somehwere/over/there/"}/>


      <Slide slideNum={1} graphicPath={"somewhere/under/there"} videoPath={"https://scontent-ord5-1.cdninstagram.com/v/t50.2886-16/277055443_254175773500571_2641974294780699781_n.mp4?efg=eyJ2ZW5jb2RlX3RhZyI6InZ0c192b2RfdXJsZ2VuLjcyMC5jYXJvdXNlbF9pdGVtLmRlZmF1bHQiLCJxZV9ncm91cHMiOiJbXCJpZ193ZWJfZGVsaXZlcnlfdnRzX290ZlwiXSJ9&_nc_ht=scontent-ord5-1.cdninstagram.com&_nc_cat=111&_nc_ohc=lCWO6EOBdJkAX90tGiX&edm=ALQROFkBAAAA&vs=17979531712492563_303780546&_nc_vs=HBksFQAYJEdOT0hneENicExEb0tfY0FBSVhrSFpLZkxhb2tia1lMQUFBRhUAAsgBABUAGCRHQWR3Z3hDOGRhRWhyZDBFQUI3NjNRZ0hsbWgyYmtZTEFBQUYVAgLIAQAoABgAGwGIB3VzZV9vaWwBMBUAACamydXJwa%2F3PxUCKAJDMywXQENMzMzMzM0YEmRhc2hfYmFzZWxpbmVfMV92MREAde4HAA%3D%3D&_nc_rid=a9d2f4c95a&ccb=7-5&oh=00_AfCd1ce6cGqOiYkS1USOPdrbVlnujWlmt-yVGZGJ_cWyzw&oe=63778BAA&_nc_sid=30a2ef"}/>
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