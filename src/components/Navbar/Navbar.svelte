<script>
  import { page } from "$app/stores";
  import Element from "./Element.svelte";
  let props = $props();
  let hidden = $state(props.hidden);
  function active(item) {
    return $page.url.pathname === `/${item.toLowerCase()}`;
  }

  function onmouseenter() {
    hidden = false;
  }
</script>

<div class="navbar" class:hidden {onmouseenter}>
  {#if !hidden}
    {#each props.items as item}
      <Element value={item} active={active(item)} />
    {/each}
  {/if}
</div>

<style>
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
  .hidden {
    height: 1rem;
  }
</style>
