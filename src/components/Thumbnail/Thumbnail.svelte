<script>
    let { src, title, description, align } = $props();
    align = align || "left";
</script>

<div class="image-container">
    <img {src} alt={title} />
    <div class="title" style="{align}: 1rem" >{title}</div>
</div>

<style>
  .image-container {
      position: relative;
      display: inline-block;
      width: 100%;
  }

  img {
      width: 100%;
      display: block;
  }

  .title {
      position: absolute;
      top: 1rem;
      color: white;
      font-family: kasper;
      text-align: right;
      font-size: 7rem;
      font-weight: bold;
  }
</style>    