<script lang="ts">
  import Header from "./Header.svelte";

  export let name: string;
</script>

<style global lang="postcss">
  /* only apply purgecss on utilities, per Tailwind docs */
  /* purgecss start ignore */
  @tailwind base;
  @tailwind components;
  /* purgecss end ignore */

  main {
    @apply text-center my-0 mx-auto;
    padding: 1em;
    max-width: 240px;
  }

  h1 {
    color: #ff3e00;
  }

  @tailwind utilities;
</style>

<main class="sm:max-w-none">
  <Header {name} />
  <p>
    Visit the
    <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
    to learn how to build Svelte apps.
  </p>
</main>
