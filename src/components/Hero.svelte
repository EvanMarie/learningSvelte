<script>
  import { goto } from "$app/navigation"; // Import the goto method

  export let title = "Evan Learns Svelte and Tailwind";
  export let tagline = "Here We Go!";
  export let buttonText = "Aaaand GO!";

  let onClick = () => {
    goto("/pageOne"); // Navigate to the desired page
  };
</script>

<header>
  <div class="hero min-h-screen bg-base-200">
    <div class="hero-content text-center">
      <div class="max-w-md">
        <h1 class="text-5xl font-bold">{title}</h1>
        <p class="py-6">{tagline}</p>
        <button class="btn btn-primary" on:click={onClick}>{buttonText}</button>
      </div>
    </div>
  </div>
</header>
