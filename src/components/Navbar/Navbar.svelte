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
    display: flex;
    justify-content: center;
    gap: 2rem;
    background-color: #f327af;
  }
</style>
