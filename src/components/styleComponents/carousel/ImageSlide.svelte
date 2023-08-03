<script>
  export let src;
  export let alt;
  // export let nextSlide;
  // export let prevSlide;
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
