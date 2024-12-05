<script>
  let { active, value } = $props();
</script>

<p class:active>
  <a href={`/${value.toLowerCase()}`}>{value}</a>
</p>

<style>
  @font-face {
    font-family: "kasper";
    src: url("arcane-nine.otf");
  }
  a {
    color: inherit;
    text-decoration: none;
  }
  p {
    color: #040103;
    display: flex;
    font-family: kasper;
    font-size: 1.8rem;
    position: relative;
    text-decoration: none;
  }
  p::after {
    content: "";
    position: absolute;
    width: 100%;
    height: 0.2rem;
    bottom: -0.4rem;
    left: 0;
    background-color: #040103;
    transform: scaleX(0);
    transform-origin: center;
    transition: transform 0.3s ease-in-out;
  }
  p:hover::after {
    transform: scaleX(1);
  }
  .active {
    color: white;
  }
  .active::after {
    background-color: white;
  }
</style>
