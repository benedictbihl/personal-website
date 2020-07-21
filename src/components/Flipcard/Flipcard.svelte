<script>
  import Front from "./Front.svelte";
  import Back from "./Back.svelte";
  import { clientHeight } from "../../stores/store.js";

  let rotate = false;
  function handleClick(event) {
    rotate = !rotate;
  }

  let clientHeight_value;

  const unsubscribe = clientHeight.subscribe(value => {
    clientHeight_value = value;
  });
</script>

<style>
  .flipcard {
    perspective: 1000px;
  }
  .flip-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.8s;
    transform-style: preserve-3d;
  }
  .flipcard.rotate .flip-card-inner {
    transform: rotateY(180deg);
  }
  .flip-button {
    z-index: 999;
    width: 39%;
    border-radius: 7px;
    position: absolute;
    right: -10px;
    padding: 0px;
    cursor: pointer;
  }

  .flip-button:hover {
    background-color: #587777;
  }

  .flip-button:focus {
    outline: none;
  }

  @media (min-width: 480px) {
    .flip-button {
      z-index: 999;
      width: 20%;
      border-radius: 7px;
      position: absolute;
      right: 0;
      padding: 3px;
      cursor: pointer;
    }
  }
</style>

<div style="height: {clientHeight_value}px" class="wrapper">
  <div class={rotate ? 'flipcard rotate' : 'flipcard'}>
    <img
      on:click={handleClick}
      class="flip-button"
      src="flip.png"
      alt="button" />
    <div class="flip-card-inner">

      <Front />
      <Back />
    </div>
  </div>

</div>
