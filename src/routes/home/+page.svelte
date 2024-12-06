<script>
  import { onMount } from "svelte";
  import NavBar from "../../components/Navbar/Navbar.svelte";

  const items = ["HOME", "COLLECTIONS", "SHOP"];
  let showNavBar = true;

  onMount(() => {
    const handleScroll = () => {
      showNavBar = window.scrollY === 0;
    }
    window.addEventListener("scroll", handleScroll);
    return () => window.removeEventListener("scroll", handleScroll);
  })
</script>

{#if showNavBar}
  <NavBar {items} />
{:else}
  <NavBar hidden/>
{/if}

<img src="collection-1.webp" alt="new collection" />

<style>
  img {
    display: flex;
    justify-self: center;
    width: 100%;
  }
</style>
