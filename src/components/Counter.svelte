<script>
  let count = 0;
  import Button from "./styleComponents/Button.svelte";
  import SectionContainer from "./styleComponents/sectionTemplateComponents/SectionContainer.svelte";

  function increment() {
    count += 1;
  }

  function decrement() {
    count -= 1;
  }
</script>

<SectionContainer exampleNo="1" title="Counter">
  <div class="counter-buttons">
    <Button text="up" onClick={increment} />
    <Button text="down" onClick={decrement} />
  </div>
  <div class="count-total-stack">
    <p>Your count is now</p>
    <div class="count">{count}</div>
  </div>
</SectionContainer>

<style>
  .counter-buttons {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 10px;
  }

  .count {
    font-size: 2em;
    font-weight: bold;
    color: deeppink;
  }

  .count-total-stack {
    display: flex;
    width: fit-content;
    flex-direction: column;
    align-items: center;
    padding: 10px;
    border-radius: 5px;
    color: white;
    justify-content: center;
    background-color: blue;
  }

  @media (min-width: 600px) {
    .counter-buttons {
      flex-direction: row;
    }
  }
</style>
