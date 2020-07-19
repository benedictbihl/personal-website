<script>
  import { onMount } from "svelte";

  import { clientHeight } from "../../stores/store.js";
  let height;
  function updateHeight() {
    clientHeight.set(height);
  }
  onMount(() => {
    updateHeight();
  });
</script>

<style>
  a {
    text-decoration: none;
    font-weight: 500;
  }
  img {
    width: 35%;
    border-radius: 50%;
  }
  p {
    margin: 1em auto;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    padding: 0;
  }

  li {
    list-style: none;
    margin: 10px 5px;
    padding: 3px 10px;
    background-color: #ff3f018a;
    border-radius: 50px;
    font-weight: 500;
    color: #230000;
  }

  .flip-card-front {
    position: absolute;
    -webkit-backface-visibility: hidden; /* Safari */
    backface-visibility: hidden;
  }

  .paragraph_strong {
    font-weight: 500;
  }

  @media (min-width: 480px) {
    img {
      width: 20%;
    }
  }
</style>

<div bind:clientHeight={height} class="flip-card-front">
  <img src="me.jpg" alt="me" />
  <p>
    My name is Benedict and I'm a web developer/technologist/UX person based in
    Munich.
    <br />
    The creative use of technology is what enables me to bring ideas to life,
    making it easy for users & clients to stop guessing if something works by
    just trying it. The web happens to be my favorite platform for that. No
    matter if as webapp, mobile app or on a smart toaster, I love building stuff
    for it. Of course I also enjoy shipping production-ready code as a change to
    rapid prototyping 😉 At the moment I´m working as Intermediate Creative
    Technologist @
    <a target="_blank" href="https://www.designaffairs.com">designaffairs</a>
    , building tangible product visions of the future.
  </p>
  <div>
    <p class="paragraph_strong">
      This is what i´ve gotten pretty good at so far:
    </p>
    <ul>
      <li>Javascript</li>
      <li>Typescript</li>
      <li>React.js</li>
      <li>Vue.js</li>
      <li>Node.js</li>
      <li>CSS/SCSS</li>
      <li>HTML5</li>
      <li>UX Concepts</li>
      <li>Wireframing</li>
      <li>Prototyping</li>
      <li>Design Ideation</li>
    </ul>
  </div>
  <div>
    <p class="paragraph_strong">
      This is what i want to learn more about in the near future:
    </p>
    <ul>
      <li>Hardware Prototyping</li>
      <li>Arduino</li>
      <li>VR/AR Development</li>
      <li>Svelte</li>
    </ul>
  </div>
</div>
