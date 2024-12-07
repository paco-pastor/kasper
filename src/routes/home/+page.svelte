<script>
  import Navbar from "../../components/Navbar/Navbar.svelte";
  import Thumbnail from "../../components/Thumbnail/Thumbnail.svelte";

  const items = ["HOME", "COLLECTIONS", "SHOP"];

</script>

<Navbar {items}/>

<Thumbnail src="collection-1.webp" title="your style" align="right"/>
<Thumbnail src="collection-2.webp" title="your rules" />
<Thumbnail src="collection-3.webp" title="kasper" align="right"/>


