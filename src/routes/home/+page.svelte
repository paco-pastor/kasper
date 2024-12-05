<script>
  import NavBar from "../../components/Navbar/Navbar.svelte";

  let items = ["HOME", "COLLECTIONS", "SHOP"];
</script>

<NavBar {items} />

<img src="collection-1.webp" alt="new collection" />

<style>
  img {
    display: flex;
    justify-self: center;
    width: 90%;
  }
</style>
