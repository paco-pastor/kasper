<script>
  import Element from "./Element.svelte";
  let props = $props();
</script>

<div class="navbar">
  {#each props.items as item}
    <Element value={item} />
  {/each}
</div>

<stye>
    .navbar {
        gap: 1em;
    }
</stye>