<script>
  import CodeExample from "../sectionTemplateComponents/CodeExample.svelte";
  import SectionContainer from "../sectionTemplateComponents/SectionContainer.svelte";
  import VisualExample from "../sectionTemplateComponents/VisualExample.svelte";
  export let carouselwidth = "300px";
</script>

<SectionContainer exampleNo="3" title="Daisy UI Carousel">
  <VisualExample>
    <div style="width: {carouselwidth};">
      <div class="carousel w-full">
        <div id="slide1" class="carousel-item relative w-full">
          <img
            src="https://placebear.com/g/200/300"
            alt="bear"
            class="w-full"
            style="border-radius: var(--radius);"
          />
          <div
            class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
          >
            <a href="#slide4" class="btn btn-circle">❮</a>
            <a href="#slide2" class="btn btn-circle">❯</a>
          </div>
        </div>
        <div id="slide2" class="carousel-item relative w-full">
          <img
            src="https://placebear.com/g/200/300"
            alt="bear"
            class="w-full"
            style="border-radius: var(--radius);"
          />
          <div
            class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
          >
            <a href="#slide1" class="btn btn-circle">❮</a>
            <a href="#slide3" class="btn btn-circle">❯</a>
          </div>
        </div>
        <div id="slide3" class="carousel-item relative w-full">
          <img
            src="https://placebear.com/g/200/300"
            alt="bear"
            class="w-full"
            style="border-radius: var(--radius);"
          />
          <div
            class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
          >
            <a href="#slide2" class="btn btn-circle">❮</a>
            <a href="#slide4" class="btn btn-circle">❯</a>
          </div>
        </div>
        <div id="slide4" class="carousel-item relative w-full">
          <img
            src="https://placebear.com/g/200/300"
            alt="bear"
            class="w-full"
            style="border-radius: var(--radius);"
          />
          <div
            class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
          >
            <a href="#slide3" class="btn btn-circle">❮</a>
            <a href="#slide1" class="btn btn-circle">❯</a>
          </div>
        </div>
      </div>
    </div></VisualExample
  >
  <CodeExample>
    {`
<div style="width: {carouselwidth};">
  <div class="carousel w-full">
    <div id="slide1" class="carousel-item relative w-full">
      <img
        src="https://placebear.com/g/200/300"
        alt="bear"
        class="w-full"
        style="border-radius: var(--radius);"
      />
      <div
        class="
          absolute 
          flex 
          justify-between
          transform 
          -translate-y-1/2 
          left-5 
          right-5 
          top-1/2"
      >
        <a href="#slide4" class="btn btn-circle">❮</a>
        <a href="#slide2" class="btn btn-circle">❯</a>
      </div>
    </div>
    <div id="slide2" class="carousel-item relative w-full">
      <img
        src="https://placebear.com/g/200/300"
        alt="bear"
        class="w-full"
        style="border-radius: var(--radius);"
      />
      <div
        class="
          absolute 
          flex 
          justify-between 
          transform 
          -translate-y-1/2 
          left-5 
          right-5 
          top-1/2"
      >
        <a href="#slide1" class="btn btn-circle">❮</a>
        <a href="#slide3" class="btn btn-circle">❯</a>
      </div>
    </div>
    <div id="slide3" class="carousel-item relative w-full">
      <img
        src="https://placebear.com/g/200/300"
        alt="bear"
        class="w-full"
        style="border-radius: var(--radius);"
      />
      <div
        class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
      >
        <a href="#slide2" class="btn btn-circle">❮</a>
        <a href="#slide4" class="btn btn-circle">❯</a>
      </div>
    </div>
    <div id="slide4" class="carousel-item relative w-full">
      <img
        src="https://placebear.com/g/200/300"
        alt="bear"
        class="w-full"
        style="border-radius: var(--radius);"
      />
      <div
        class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2"
      >
        <a href="#slide3" class="btn btn-circle">❮</a>
        <a href="#slide1" class="btn btn-circle">❯</a>
      </div>
    </div>
  </div>
  </div>`}
  </CodeExample>
</SectionContainer>
