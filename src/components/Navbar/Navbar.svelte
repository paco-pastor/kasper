<script>
  import { onMount } from "svelte";
  import { slide } from "svelte/transition";
  import { page } from "$app/stores";
  import Element from "./Element.svelte";

  let props = $props();
  let hidden = $state(false);

  function active(item) {
    return $page.url.pathname === `/${item.toLowerCase()}`;
  }

  function onmouseenter() {
    hidden = false;
  }

  onMount(() => {
    const handleScroll = () => {
      hidden = window.scrollY > 0;
    };
    window.addEventListener("scroll", handleScroll);
    return () => window.removeEventListener("scroll", handleScroll);
  });
</script>

{#if !hidden}
  <div class="navbar" transition:slide>
    {#each props.items as item}
      <Element value={item} active={active(item)} />
    {/each}
  </div>
{:else}
  <div class="navbar minified" transition:slide {onmouseenter}></div>
{/if}

<style>
  .minified {
    height: 1rem;
  }
  .navbar {
    background-color: #f327af;
    display: flex;
    color: white;
    gap: 2rem;
    justify-content: center;
    position: sticky;
    text-align: center;
    top: 0;
    z-index: 100;
  }
</style>
