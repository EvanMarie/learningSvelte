<script>
  import Carousel from "./styleComponents/carousel/Carousel.svelte";
  import CodeExample from "./styleComponents/sectionTemplateComponents/CodeExample.svelte";
  import SectionContainer from "./styleComponents/sectionTemplateComponents/SectionContainer.svelte";
  import VisualExample from "./styleComponents/sectionTemplateComponents/VisualExample.svelte";
</script>

<SectionContainer exampleNo="4" title="My Carousel Component">
  <VisualExample style="border-radius: 10px">
    <Carousel carouselwidth="300px" /></VisualExample
  >
  <CodeExample
    >{`
/* Carousel.svelte */
<script>
  import ImageSlide from "./ImageSlide.svelte";
  export let carouselwidth = "300px";
  export let images = [];
</script>

<div style="width: {carouselwidth};">
  <div class="carousel w-full">
    {#each images as image, index}
      <ImageSlide
        src={image.src}
        alt={image.alt}
        nextSlide={"#slide" + (((index + 1) % images.length) + 1)}
        prevSlide={"#slide" +
          (((index - 1 + images.length) % images.length) + 1)}
      />
    {/each}
  </div>
</div>

/* ImageSlide.svelte */

<script>
  export let src;
  export let alt;
</script>

<div class="carousel-item relative w-full">
  <img
    {src}
    {alt}
    class="w-full"
    style="border-radius: var(--radius); postition: relative"
  />
  <div style="position: absolute; bottom: 0; left: 50%;" />
</div>
`}
  </CodeExample>
</SectionContainer>
