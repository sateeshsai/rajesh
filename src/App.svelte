<script>
  import Home from "./Home.svelte";
  import Testimonials from "./Testimonials.svelte";

  let active = "home";
</script>

<svelte:head>
  <title>Rajesh Sambu farewell</title>
  <style>
    @import url("https://rsms.me/inter/inter.css");
    @import url("https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@200;300&family=Inter:wght@300;900&display=swap");
  </style>
</svelte:head>

<main>
  {#if active === "home"}
    <Home on:click={() => (active = "testimonials")} />
  {:else}
    <Testimonials />
  {/if}
</main>

<style>
  :global(html, body) {
    font-size: clamp(7px, calc(0.35vw + 0.35vh + 0.15vmin), 20px);
    font-family: "Inter", sans-serif;
    margin: 0;
    padding: 0;
    --backgroundColorHome: #1c1c26;
    --textColor: #eeedff;
    --dColor: #86bc25;
    --footerColor: #9eadbd;
    --accentColor: #7888f3;
  }

  :global(::-webkit-scrollbar) {
    background: var(--backgroundGreyColor);
    border-radius: 1rem;
    width: 0rem;
  }
  :global(::-webkit-scrollbar-thumb) {
    background-color: #a5b3c6;
    border-radius: 1rem;
  }
</style>
