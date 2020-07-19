<script>
  import LinkBar from "../components/LinkBar.svelte";
</script>

<style>
  :global(body) {
    background-color: #668b8b;
    color: #212020;
  }
  main {
    position: relative;
    max-width: 60em;
    padding: 2em;
    margin: 0 auto;
    box-sizing: border-box;
  }
</style>

<main>
  <slot />
</main>
<LinkBar />
