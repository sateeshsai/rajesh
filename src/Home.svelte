<script>
  import Left from "./Back.svelte";
  import { flip } from "svelte/animate";
  import { fly, fade, slide } from "svelte/transition";
  import { quintInOut } from "svelte/easing";
  import { crossfade } from "svelte/transition";
  const [send, receive] = crossfade({});

  let showLargePic = false;
  //   export let iconBackgroundColor;
  //   export let iconColor;
  //   export let itemIconOpacity;
  //   export let iconStrokeWidth;

  let picHolder = [{ id: 1, src: "/images/home.png" }];
  let largePicHolder = [{ id: 1, src: "/images/home.png" }];
</script>

<div class="home" transition:slide={{ easing: quintInOut }}>
  {#if !showLargePic}
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
      {#each picHolder as pic (pic.id)}
        <div class="pic" animate:flip in:receive={{ key: pic, duration: 200 }} out:send={{ key: pic, duration: 200 }}>
          <img on:click={() => (showLargePic = true)} src={pic.src} alt="Rajesh's portrait collage" />
        </div>
      {/each}
    </div>
  {/if}
</div>

{#if showLargePic}
  {#each picHolder as pic (pic.id)}
    <div class="largePic" animate:flip in:receive={{ key: pic, duration: 200 }} out:send={{ key: pic, duration: 200 }}>
      <img on:click={() => (showLargePic = true)} src={pic.src} alt="Rajesh's portrait collage" />
      <div class="byWrapper a"><div class="by "><span>By</span> Minal</div></div>
      <div class="byWrapper b"><div class="by  "><span>By</span> Eesha</div></div>
      <div class="byWrapper c"><div class="by "><span>By</span> Kashyap</div></div>
      <div class="byWrapper ca"><div class="by "><span>By</span> Nitesh</div></div>
      <div class="byWrapper Shweta"><div class="by"><span>By</span> Shweta</div></div>
      <div class="byWrapper d"><div class="by "><span>By</span> Tripti G</div></div>
      <div class="byWrapper e"><div class="by "><span>By</span> Mohit</div></div>
      <div class="byWrapper f"><div class="by "><span>By</span> Tripti R</div></div>
      <div class="byWrapper g"><div class="by "><span>By</span> Rakesh</div></div>
    </div>
  {/each}
  <button class="close" on:click={() => (showLargePic = false)}>X</button>
{/if}

<style>
  .home {
    display: grid;
    grid-template-columns: 1fr 50vw;
    /* border: 1px solid red; */
    height: 100vh;
    overflow: hidden;
    background: var(--backgroundColorHome);
    grid-area: main;
  }

  .largePic {
    /* position: absolute; */
    /* top: 0; */
    height: 100%;
    /* width: 100%; */
    display: grid;
    place-items: center;
    background: var(--backgroundColorHome);
    grid-area: main;
  }

  .largePic img {
    height: 100vh;
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
    background-color: var(--backgroundColorHome);
  }

  .right {
    justify-self: end;
    width: 50vw;
    display: grid;
    justify-content: center;
    align-items: center;
    height: 100vh;
    position: relative;
    /* border-radius: 1rem; */
    overflow: hidden;
  }

  .right img {
    height: 100vh;
    position: relative;
    right: -5rem;
    cursor: pointer;
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

  .byWrapper {
    position: absolute;
    /* border: 5px solid red; */
    display: grid;
    place-items: center;
    opacity: 0;
  }

  .byWrapper:hover {
    opacity: 1;
  }

  .a {
    left: 0%;
    top: 0%;
    height: 33%;
    width: 25%;
  }

  .b {
    left: 0%;
    top: 36%;
    height: 30%;
    width: 42%;
  }

  .c {
    right: 0%;
    top: 38%;
    height: 35%;
    width: 35%;
  }

  .ca {
    right: 35%;
    top: 35%;
    height: 33%;
    width: 20%;
  }

  .d {
    left: 0%;
    bottom: 0%;
    height: 31%;
    width: 32%;
  }

  .e {
    right: 41%;
    bottom: 0%;
    height: 35%;
    width: 25%;
  }

  .f {
    right: 0%;
    top: 0%;
    height: 33%;
    width: 35%;
  }

  .g {
    right: 0%;
    bottom: 0%;
    height: 28%;
    width: 43%;
  }

  .Shweta {
    left: 25%;
    top: 0%;
    height: 33%;
    width: 38%;
  }

  .by {
    top: 0;
    font-size: 2rem;
    font-weight: 800;
    background: var(--backgroundColorHome);
    font-family: "IBM Plex Mono", monospace;
    padding: 0.8rem;
    border: 1px solid white;
    box-shadow: rgb(38, 57, 77) 0px 20px 30px -10px;
  }

  .by span {
    color: var(--accentColor);
    font-weight: 300;
  }

  .close {
    position: absolute;
    top: 0;
    right: 0;
    margin: 3rem;
    font-size: 2rem;
    display: grid;
    place-items: center;
    color: white;
  }
</style>
