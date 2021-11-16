<script>
  import P5 from "../components/P5.svelte";
  let w, h;
  const sketch = p5 => {
    p5.setup = () => {
      p5.createCanvas(w, h);
    };

    p5.draw = () => {
      p5.ellipse(p5.mouseX, p5.mouseY, 50, 50);
    };
  };
</script>
<svelte:window 
  bind:innerWidth={w} 
  bind:innerHeight={h}
/>
<P5 {sketch} />