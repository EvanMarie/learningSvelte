<div class="visual-example">
  <slot />
</div>

<style>
  .visual-example {
    width: 100%;
    max-width: 400px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
  }

  @media (min-width: 700px) {
    .visual-example {
      max-width: 650px;
    }
  }

  @media (min-width: 900px) {
    .visual-example {
      width: 100%;
      max-width: 425px;
    }
  }

  @media (min-width: 1200px) {
    .visual-example {
      max-width: 550px;
    }
  }
</style>
