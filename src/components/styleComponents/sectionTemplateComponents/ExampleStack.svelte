<div class="example-code-stack">
  <slot />
</div>

<style>
  @media (min-width: 0px) {
    .example-code-stack {
      width: 100%;
      max-width: 400px;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      align-items: center;
      justify-content: center;
    }
  }

  @media (min-width: 700px) {
    .example-code-stack {
      max-width: 680px;
    }
  }

  @media (min-width: 900px) {
    .example-code-stack {
      flex-direction: row;
      max-width: 875px;
    }
  }

  @media (min-width: 1200px) {
    .example-code-stack {
      max-width: 1150px;
    }
  }
</style>
