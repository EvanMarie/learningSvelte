<script>
  let fontSize = "1.5em";
  let color = "cyan";
  export let exampleNo = "";
  export let title = "";
</script>

<div class="section-container">
  <div class="section-title" style="font-size: {fontSize}; color: {color};">
    Example No: {exampleNo} - {title}
  </div>
  <div class="example-container">
    <slot />
  </div>
</div>

<style>
  .section-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    gap: 10px;
    border-bottom: 1px solid rgba(100, 100, 100, 0.6);
    width: 100%;
    padding-bottom: 20px;
  }

  .section-title {
    width: 100%;
    text-align: left;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    padding: 0px 10px 20px 10px;
  }

  .example-container {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    gap: 20px;
  }
</style>
