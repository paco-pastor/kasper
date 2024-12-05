<script>
  let props = $props();
</script>

<p>{props.value}</p>

<style>
  @font-face {
    font-family: "kasper";
    src: url("arcane-nine.otf");
  }
  p {
    display: inline-block;
    font-family: kasper;
    font-size: 3em;
    position: relative;
    text-decoration: none;
  }
  p::after {
    content: "";
    position: absolute;
    width: 100%;
    height: 2px;
    bottom: -4px;
    left: 0;
    background-color: black;
    transform: scaleX(0);
    transform-origin: center;
    transition: transform 0.3s ease-in-out;
  }
  p:hover::after {
    transform: scaleX(1);
  }
</style>
