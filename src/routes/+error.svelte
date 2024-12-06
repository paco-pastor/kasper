<script>
  import { page } from "$app/stores";
</script>

{#if $page.status === 404}
  <div>
    <img src="404.jpg" alt="404"/>
  </div>
{/if}

<style>
  img {
    height: 30vh;
  }
  div {
    background-color: #f327af;
    display: flex;
    height: 100vh;
    justify-content: center;
    align-items: center;
  }
</style>
