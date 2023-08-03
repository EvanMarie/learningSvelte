<script>
  let count = 0;
  import Button from "./styleComponents/Button.svelte";
  import CodeExample from "./styleComponents/sectionTemplateComponents/CodeExample.svelte";
  import ExampleStack from "./styleComponents/sectionTemplateComponents/ExampleStack.svelte";
  import SectionContainer from "./styleComponents/sectionTemplateComponents/SectionContainer.svelte";
  import VisualExample from "./styleComponents/sectionTemplateComponents/VisualExample.svelte";

  function increment() {
    count += 1;
  }

  function decrement() {
    count -= 1;
  }
</script>

<SectionContainer exampleNo="1" title="Counter">
  <VisualExample>
    <div class="counter-buttons">
      <Button text="up" onClick={increment} />
      <Button text="down" onClick={decrement} />
    </div>
    <div class="count-total-stack">
      <p>Your count is now</p>
      <div class="count">{count}</div>
    </div></VisualExample
  >
  <CodeExample
    >{`<div class="counter-buttons">
        <Button text="up" onClick={increment} />
        <Button text="down" onClick={decrement} />
      </div>
      <div class="count-total-stack">
        <p>Your count is now</p>
        <div class="count">{count}</div>`}</CodeExample
  >
</SectionContainer>

<style>
  .counter-buttons {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: center;
    flex-direction: row;
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
    padding: 20px;
    border-radius: 5px;
    color: white;
    justify-content: center;
    background-color: darkcyan;
  }
</style>
