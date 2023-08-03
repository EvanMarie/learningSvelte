<script>
  import Carousel from "./styleComponents/carousel/Carousel.svelte";
  import SectionContainer from "./styleComponents/sectionTemplateComponents/SectionContainer.svelte";
  const images = [
    { src: "https://picsum.photos/id/123/200", alt: "image" },
    { src: "https://picsum.photos/id/144/200", alt: "image" },
    { src: "https://picsum.photos/id/153/200", alt: "image" },
    { src: "https://picsum.photos/id/188/200", alt: "image" },
  ];
</script>

<SectionContainer exampleNo="3" title="Image Carousel">
  <Carousel {images} carouselwidth="300px" />
</SectionContainer>
