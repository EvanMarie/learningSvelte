<script>
  import PageContainer from "./PageContainer.svelte";
  import PageHeading from "./PageHeading.svelte";
  export let fontSize = "3em";
  export let color = "deeppink";
  export let title = "";
</script>

<PageContainer>
  <PageHeading {fontSize} {color} {title} />

  <div class="content">
    <slot />
  </div>
</PageContainer>

<style>
  .content {
    padding-top: 20px;
    width: 100%;
    max-width: 1200px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    gap: 20px;
  }
</style>
