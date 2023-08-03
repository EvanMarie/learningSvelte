<!-- Button.svelte -->
<script>
  // Define props with default values
  export let text = "Button";
  export let variant = "primary";
  export let size = "medium";
  export let onClick = () => {};

  // Define the button classes based on props
  const buttonClasses = `
    button
    ${variant === "primary" ? "primary-button" : "secondary-button"}
    ${size === "small" ? "small-button" : "medium-button"}
  `;
</script>

<button class={buttonClasses} on:click={onClick}>{text}</button>

<style>
  /* Component-specific styles */
  .button {
    cursor: pointer;
    padding: 2px 10px;
    border: none;
    border-radius: 4px;
    color: black;
    border: 2px solid black;
    box-shadow: 1px 1px 3px darkslategray;
    font-size: 16px;
  }

  .primary-button {
    background-color: cyan;
  }

  .secondary-button {
    background-color: #6c757d;
  }

  .small-button {
    font-size: 14px;
  }
</style>
