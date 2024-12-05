<script>
  import NavBar from "../components/Navbar/Navbar.svelte";

    let items = ["Home", "About", "Contact"];
</script>

<NavBar {items} />

<img src="collection-1.webp" alt="new collection">

<style>
    img {
        width: 100%;
    }
</style>
