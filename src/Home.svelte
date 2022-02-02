<script>
  import Left from "./Back.svelte";
  import { fly, fade, slide } from "svelte/transition";
  import { quintInOut } from "svelte/easing";

  //   export let iconBackgroundColor;
  //   export let iconColor;
  //   export let itemIconOpacity;
  //   export let iconStrokeWidth;
</script>

<div class="home" transition:slide={{ easing: quintInOut }}>
  <div class="left">
    <h1>For you are<br /> a jolly good fellow.</h1>
    <div class="leftBottom">
      <h2>With <span>❤</span> from your Deloitte friends</h2>

      <button class="go" on:click>
        <Left iconBackgroundColor="var(--textColor)" iconColor="white" itemIconOpacity="0" iconStrokeWidth="20" />
      </button>
    </div>
  </div>

  <div class="right">
    <img src="/images/home.jpg" alt="Rajesh's portrait collage" />
  </div>
</div>

<style>
  .home {
    display: grid;
    grid-template-columns: 4fr 1fr;
    /* border: 1px solid red; */
    height: 100vh;
    overflow: hidden;
    background-color: var(--backgroundColorHome);
  }

  h1 {
    font-family: "Inter", sans-serif;
    font-size: 8rem;
    letter-spacing: -0.25rem;
    line-height: 9rem;
  }

  h2 {
    font-family: "IBM Plex Mono", monospace;
    font-size: 2rem;
    line-height: 2rem;
    color: var(--footerColor);
  }

  h2 span {
    /* color: var(--dColor); */
    font-size: 3rem;
  }

  .left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 10rem;
    color: var(--textColor);
    gap: 4rem;
  }

  .right {
    justify-self: end;
    width: 50vw;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  .right img {
    height: 100vh;
  }

  .leftBottom {
    display: flex;
    align-items: center;
    gap: 2rem;
  }

  button {
    width: 4rem;
    height: 4rem;
    background: var(--accentColor);
    border: none;
    border-radius: 3rem;
    transition: all 0.2s ease-in-out;
    cursor: pointer;
  }

  button:hover {
    transform: scale(1.3);
  }
</style>
