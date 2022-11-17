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
    {slideNum: 0, title: "Exploring is Beautiful", imagePath: "/imgs/humber-pond-2022-10-31.jpg", caption: "Autumn (Humber pond. Oct, 2022)"},
    {slideNum: 1, title: "Exploring is Beautiful", imagePath: "/imgs/cool-tree.jpg", caption: "Cool Roots. (Cootes paradise. Jan, 2021)"},
    {slideNum: 2, title: "Exploring is Ugly", imagePath: "/imgs/shopping-cart-2022-04-17.jpg", caption: "We Live in A Society. (Brampton pond. Apr, 2022)"},
    {slideNum: 3, title: "Exploring is Sad", imagePath: "/imgs/abandoned-teddy-2022-10-12.jpg", caption: "A Loss Too Great To Bear. (Brampton. Oct, 2022)"},
    {slideNum: 4, title: "Exploring is Intriguing", imagePath: "/imgs/forbidden-hottub.jpg", caption: "Forbidden Hot Tub. (Brampton pond. Sep, 2022)"},
    {slideNum: 5, title: "Intriguing: What's the Story?", imagePath: "/imgs/humber-pumpkins-2022-10-31.jpg", caption: "Pumpkin Party. (Humber. Oct, 2022)"},
    {slideNum: 6, title: "Intriguing: How was that made?", imagePath: "/imgs/weird-spiderweb-2021-08-28.jpg", caption: "Weird, Wide, Web. (Aug, 2021)"},
    {slideNum: 7, title: "Intriguing: ..., why?", videoPath: "https://scontent-ord5-1.cdninstagram.com/v/t50.2886-16/277055443_254175773500571_2641974294780699781_n.mp4?efg=eyJ2ZW5jb2RlX3RhZyI6InZ0c192b2RfdXJsZ2VuLjcyMC5jYXJvdXNlbF9pdGVtLmRlZmF1bHQiLCJxZV9ncm91cHMiOiJbXCJpZ193ZWJfZGVsaXZlcnlfdnRzX290ZlwiXSJ9&_nc_ht=scontent-ord5-1.cdninstagram.com&_nc_cat=111&_nc_ohc=lCWO6EOBdJkAX90tGiX&edm=ALQROFkBAAAA&vs=17979531712492563_303780546&_nc_vs=HBksFQAYJEdOT0hneENicExEb0tfY0FBSVhrSFpLZkxhb2tia1lMQUFBRhUAAsgBABUAGCRHQWR3Z3hDOGRhRWhyZDBFQUI3NjNRZ0hsbWgyYmtZTEFBQUYVAgLIAQAoABgAGwGIB3VzZV9vaWwBMBUAACamydXJwa%2F3PxUCKAJDMywXQENMzMzMzM0YEmRhc2hfYmFzZWxpbmVfMV92MREAde4HAA%3D%3D&_nc_rid=a96ccc9f0c&ccb=7-5&oh=00_AfCd1ce6cGqOiYkS1USOPdrbVlnujWlmt-yVGZGJ_cWyzw&oe=63778BAA&_nc_sid=30a2ef", caption: "Basement Surprise. (Hamilton. Mar, 2022)"},
    {slideNum: 8, title: "Exploring Isn't Always Safe", imagePath: "/imgs/climbing-electrical-towers-2022-03-18.jpg", caption: "'I'm in Electrical Engineering, don't worry' (Hamilton. Mar, 2022)"},
    {slideNum: 9, title: "Exploring Isn't Always Safe...", imagePath: "/imgs/jumping-fences-2022-04-15.jpg", caption: "TL;DR: Accidentally trapped myself by a highway, jumped a fence, and ripped my shirt - while carrying a slightly stale, but delicious, 12\" pizza from Papa John's - so I could catch a bus to my friend's place. (Hamilton. Apr, 2022)"},
    {slideNum: 10, title: "Exploring = Freedom", imagePath: "/imgs/brampton-sidewalk-2022-09.jpg", caption: "On the Road to Somewhere. (Brampton. Sep, 2022)"},
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
      <TitleSlide title={"The End"} subtitle={"Thanks for your time :)"} author={""}/>
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