<div class="code-example">
  <div class="mockup-code">
    <pre style="padding: 0px 30px; color: pink"><code><slot /></code></pre>
  </div>
</div>

<style>
  .code-example {
    width: 100%;
    max-width: 375px;
    height: 100%;
    max-height: 375px;
    overflow-y: auto;
    text-align: left;
    font-size: 70%;
    border-radius: 15px;
  }

  @media (min-width: 700px) {
    .code-example {
      max-width: 450px;
      font-size: 80%;
    }
  }

  @media (min-width: 900px) {
    .code-example {
      width: 100%;
      max-width: 425px;
      font-size: 90%;
    }
  }

  @media (min-width: 1200px) {
    .code-example {
      max-width: 550px;
    }
  }
</style>
