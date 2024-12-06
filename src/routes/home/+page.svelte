<script>
  import Navbar from "../../components/Navbar/Navbar.svelte";

  const items = ["HOME", "COLLECTIONS", "SHOP"];

</script>

<Navbar {items}/>

<img src="collection-1.webp" alt="new collection" />
<img src="collection-2.webp" alt="new collection" />
<img src="collection-3.webp" alt="new collection" />

<style>
  img {
    display: flex;
    justify-self: center;
    width: 100%;
  }
</style>
