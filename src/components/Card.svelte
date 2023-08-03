<script>
  import CodeExample from "./styleComponents/sectionTemplateComponents/CodeExample.svelte";
  import SectionContainer from "./styleComponents/sectionTemplateComponents/SectionContainer.svelte";
  import VisualExample from "./styleComponents/sectionTemplateComponents/VisualExample.svelte";

  export let title = "Card Title";
  export let descirption = "Card Description";
  export let buttonText = "Button Text";
  export let image = "http://picsum.photos/seed/picsum/390";
</script>

<SectionContainer exampleNo="5" title="Card Component">
  <VisualExample>
    <div class="card w-80 glass">
      <figure>
        <img src={image} alt="example" />
      </figure>
      <div class="card-body">
        <h2 class="card-title">{title}</h2>
        <p>{descirption}</p>
        <div class="card-actions justify-end">
          <button class="btn btn-primary">{buttonText}</button>
        </div>
      </div>
    </div>
  </VisualExample>

  <CodeExample
    >{`
<script>
  import CodeExample from "./styleComponents/sectionTemplateComponents/CodeExample.svelte";
  import SectionContainer from "./styleComponents/sectionTemplateComponents/SectionContainer.svelte";
  import VisualExample from "./styleComponents/sectionTemplateComponents/VisualExample.svelte";

  export let title = "Card Title";
  export let descirption = "Card Description";
  export let buttonText = "Button Text";
  export let image = "http://picsum.photos/seed/picsum/390";
</script>
<div class="card w-96 glass">
    <figure>
    <img src={image} alt="example" />
    </figure>
    <div class="card-body">
    <h2 class="card-title">{title}</h2>
    <p>{descirption}</p>
    <div class="card-actions justify-end">
        <button class="btn btn-primary">{buttonText}</button>
    </div>
    </div>
</div>`}</CodeExample
  >
</SectionContainer>
