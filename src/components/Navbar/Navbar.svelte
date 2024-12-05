<script>
  import { page } from "$app/stores";
  import Element from "./Element.svelte";
  let props = $props();

  function active(item) {
    return $page.url.pathname === `/${item.toLowerCase()}`;
  }
</script>

<div class="navbar">
  {#each props.items as item}
    <Element value={item} active={active(item)} />
  {/each}
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
</style>
