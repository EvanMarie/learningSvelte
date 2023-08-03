<!-- PageHeading.svelte -->
<script>
  export let fontSize;
  export let color;
  export let title;
</script>

<div class="heading-container">
  <div class="page-heading" style="font-size: {fontSize}; color: {color};">
    <div class="flex flex-col w-full border-opacity-50">
      <div class="divider">{title}</div>
    </div>
  </div>
</div>

<style>
  .heading-container {
    width: 100%;
    max-width: 1000px;
    padding-bottom: 20px;
  }
  .page-heading {
    display: flex;
    width: 100%;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-shadow: var(--darkShadow);
  }
</style>
