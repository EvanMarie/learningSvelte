<script>
  import Button from "./styleComponents/Button.svelte";
  export let task = "";
  export let remove = () => {};
</script>

<div>
  {#if task}
    <div class="todo-item">
      <span>{task}</span>
      <Button text="remove" onClick={remove} />
    </div>
  {:else}
    <span>No task</span>
  {/if}
</div>

<style>
  .todo-item {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.3);
    padding: 5px 10px;
    margin-bottom: 10px;
  }
</style>
