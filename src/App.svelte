<script lang="ts">
  import TitleSlide from './lib/TitleSlide.svelte';
  import Slide from './lib/Slide.svelte';

  let numSlides = 5;
  let slideIndices = [...Array(numSlides).keys()];

  let options = {
    root: document.querySelector('main'),
    rootMargin: '0px',
    threshold: 1.0,
  }

  let callback: IntersectionObserverCallback = (entries, observer) => {
    entries.forEach((entry) => {
      console.log(entry);
      if (entry.isIntersecting) {
        (entry.target as HTMLElement).style.opacity = '1.0';
      } else if (!entry.isIntersecting) {
        (entry.target as HTMLElement).style.opacity = '0.0';
      }
    });
  }

  let myObserver = new IntersectionObserver(callback, options);

  // TODO: Move observer to store
  // TODO: Create multiple types of observers for different effects:
  /*  Fade observer
  */
</script>

<main>
  <TitleSlide />

  <Slide observer={myObserver} slideNum={0} graphicPath="somehwere/over/there/"/>
  <Slide observer={myObserver} slideNum={1} graphicPath="somehwere/under/where/"/>

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