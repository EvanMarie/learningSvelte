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
