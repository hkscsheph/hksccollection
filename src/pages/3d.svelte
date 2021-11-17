<!-- Ref: https://levelup.gitconnected.com/3d-with-svelte-and-babylon-js-4f9387728d35 -->
<script>
  import { onMount } from "svelte";
  import { createScene } from "../lib/scene";
  let el;
  onMount(() => {
    createScene(el);
  });
</script>

<canvas bind:this={el}></canvas>

<style>
  canvas {
    width: 100vw;
    height: calc(100vh - 30px);
    display: block;
  }
</style>