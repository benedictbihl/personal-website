<script>
  import Flipcard from "../components/Flipcard/Flipcard.svelte";
  import LinkBar from "../components/LinkBar.svelte";
</script>

<style>
  h1 {
    text-align: center;
    margin: 0 auto;
    font-size: 1.8em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
</style>

<svelte:head>
  <title>Benedict Bihlmaier | Developer & Technologist</title>
</svelte:head>
<h1>Hey you! Thanks for stopping by</h1>
<Flipcard />
<LinkBar />
