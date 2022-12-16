<script>
  import "chota";
  import "../app.css";
  import { onMount } from "svelte";

  // Set dark mode if it is preferred
  onMount(() => {
    if (
      window.matchMedia &&
      window.matchMedia("(prefers-color-scheme: dark)").matches
    ) {
      document.body.classList.add("dark");
    }
  });
</script>

<nav class="nav">
  <div class="nav-center">
    <div class="tabs">
      <a href="/">Home</a>
      <a href="/about">About</a>
    </div>
  </div>
</nav>

<div class="container">
  <slot />
</div>
