<script>
  import ImageSlide from "./ImageSlide.svelte";
  export let carouselwidth = "300px";
  export let images = [
    { src: "https://picsum.photos/id/123/200", alt: "image" },
    { src: "https://picsum.photos/id/144/200", alt: "image" },
    { src: "https://picsum.photos/id/153/200", alt: "image" },
    { src: "https://picsum.photos/id/188/200", alt: "image" },
    { src: "https://picsum.photos/id/193/200", alt: "image" },
    { src: "https://picsum.photos/id/222/200", alt: "image" },
    { src: "https://picsum.photos/id/111/200", alt: "image" },
    { src: "https://picsum.photos/id/12/200", alt: "image" },
    { src: "https://picsum.photos/id/33/200", alt: "image" },
    { src: "https://picsum.photos/id/15/200", alt: "image" },
    { src: "https://picsum.photos/id/19/200", alt: "image" },
  ];
</script>

<h2 style="font-size: 20px;">← Swipe →</h2>
<div style="width: {carouselwidth}; border-radius: 10px;">
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
