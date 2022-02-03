<script>
  import Left from "./Back.svelte";
  import Tests from "./Tests.svelte";
  import { fly, fade, slide } from "svelte/transition";
  import { quintInOut } from "svelte/easing";
  import Masonry from "svelte-bricks";

  let items = [
    { id: 1, src: "/images/1.jpg" },
    { id: 2, src: "/images/2.jpg" },
    { id: 3, src: "/images/3.jpg" },
    { id: 4, src: "/images/4.jpg" },
    { id: 5, src: "/images/5.jpg" },
    { id: 6, src: "/images/6.jpg" },
    { id: 7, src: "/images/7.jpg" },
    { id: 8, src: "/images/8.jpg" },
    { id: 9, src: "/images/9.jpg" },
    { id: 10, src: "/images/10.jpg" },
    { id: 11, src: "/images/11.jpg" },
    { id: 12, src: "/images/12.jpg" },
    { id: 13, src: "/images/13.jpg" },
    { id: 14, src: "/images/14.jpg" },
    { id: 15, src: "/images/15.jpg" },
  ];

  let [minColWidth, maxColWidth, gap] = [200, 900, 20];
  let width, height;

  let showPicframe = false;

  let selectedPicSrc;

  let dim = false;

  function showPicture(id) {
    showPicframe = true;
    selectedPicSrc = `/images/${id}.jpg`;
    dim = true;
  }

  function closePicture() {
    showPicframe = false;
    dim = false;
    selectedPicSrc = "";
  }
</script>

<div class="mainContainer">
  <div class="container" transition:slide={{ easing: quintInOut }}>
    <div class="left-right">
      <div class="left" class:dim>
        <div class="top">
          <div class="topLeft">
            <h1>We wish you the best</h1>
            <h2><span>and</span> we will miss you.</h2>
          </div>
          <div class="topRight" />
        </div>
        <div class="seperator" />
        <div class="bottom">
          <Tests />
        </div>
      </div>
      {#if showPicframe}
        <div class="picFrame">
          <img transition:fade src={selectedPicSrc} alt="selected" />
          <button class="close" on:click={closePicture}>X</button>
        </div>
      {/if}
      <div class="right">
        <Masonry {items} {minColWidth} {maxColWidth} {gap} let:item bind:width bind:height>
          <img on:click={() => showPicture(item.id)} src={item.src} alt="" />
        </Masonry>
      </div>
    </div>
  </div>
</div>

<div class="footer">
  <div class="homeButton" on:click>Home</div>
  <div>With <span>❤</span> from your Deloitte friends</div>
</div>

<style>
  .mainContainer {
    display: grid;
  }

  .container {
    /* display: grid; */
    /* grid-template-columns: 2fr 1fr; */
    /* border: 1px solid red; */
    height: 96vh;
    overflow: hidden;
    background-color: var(--backgroundColorHome);
  }

  .left-right {
    display: grid;
    grid-template-columns: 2fr 1fr;
    /* grid-area: test; */
    /* grid-template-areas: "test"; */
    position: relative;
  }

  .picFrame {
    /* grid-area: test; */
    width: 66%;
    height: 100%;
    display: grid;
    place-items: center;
    /* position: relative; */
    position: absolute;
    z-index: 999;
  }

  .picFrame img {
    width: 70rem;
    max-width: 80%;
    border-radius: 2rem;
    box-shadow: rgba(0, 0, 0, 0.12) 0px 1px 3px, rgba(0, 0, 0, 0.24) 0px 1px 2px;
    position: relative;
    /* top: -3rem; */
  }

  .left {
    display: flex;
    flex-direction: column;
    /* grid-template-rows: 2fr 20vh 2rem; */
    gap: 2rem;
    padding: 5rem;
    max-height: 95vh;
    overflow: scroll;
    transition: all 0.2s ease;
  }

  h1,
  h2 {
    margin: 0;
    font-size: 7rem;
    letter-spacing: -0.2rem;
  }
  h1 {
    color: var(--accentColor);
  }

  h2 {
    position: relative;
    top: -1.5rem;
    letter-spacing: -0.1rem;
  }

  h2 span {
    font-weight: 200;
  }

  .right {
    background: grey;
    margin-bottom: 5rem;
    max-height: 95vh;
  }

  .top {
    display: grid;
    grid-template-columns: 5fr 1fr;
    align-self: start;
  }

  .bottom {
    display: grid;
    /* grid-template-columns: repeat(3, 1fr); */
    gap: 4rem;
    overflow: scroll;
    margin-bottom: 5rem;
  }

  .footer {
    font-family: "IBM Plex Mono", monospace;
    background: var(--accentColor);
    height: 4vh;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-right: 2rem;
    padding-left: 5rem;
    font-size: 1.2rem;
  }

  .right {
    display: grid;
    align-items: start;
    height: 100vh;
    overflow: scroll;
    padding: 2rem;
    background: #484753;
  }

  .right img {
    max-width: 100%;
    border-radius: 0.5rem;
    transition: all 0.2s ease-in-out;
    cursor: pointer;
  }

  .right img:hover {
    transform: scale(1.03);
    box-shadow: rgba(255, 255, 255, 0.1) 0px 1px 1px 0px inset, rgba(50, 50, 93, 0.25) 0px 50px 100px -20px,
      rgba(0, 0, 0, 0.3) 0px 30px 60px -30px;
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

  .seperator {
    height: 1rem;
    background: var(--accentColor);
  }

  .homeButton {
    cursor: pointer;
    color: var(--backgroundColorHome);
    font-weight: 600;
  }

  .close {
    position: absolute;
    top: 0;
    right: 0;
    margin: 5rem;
    font-size: 1.5rem;
    display: grid;
    place-items: center;
    color: white;
    padding: 1rem;
  }

  .dim {
    filter: saturate(0) blur(0.2rem);
    opacity: 0.3;
  }
</style>
