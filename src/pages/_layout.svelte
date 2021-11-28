<!-- routify:options preload="proximity" -->
<script>
  let expand = false;
</script>
<!-- <nav> is for nav bar -->
<nav class:expand>
	<a href="/"> Home </a>
	<a href="/about"> About </a>
	<a href="/portfolio"> Portfolio </a>
	<a href="/video"> Video </a>
	<a href="/scroll"> Scroll </a>
	<a href="/drag"> Drag </a>
	<a href="/cat"> Cat </a>
	<a href="/chart"> Chart </a>
	<a href="/p5"> P5 </a>
	<a href="/3d"> 3D </a>
	<button on:click={e => expand = !expand}> Expand </button>
</nav>
<!-- <slot /> is for page content -->
<main>
	<slot />
</main>

<style>
  nav {
    z-index: 1;
    background-color: pink;
    position: fixed;
    height: 30px;
    width: 100%;
    transition: 1s;
  }
  nav.expand {
    width: 20%;
    height: 100vh;
    display: flex;
    flex-direction: column;
  }
  nav button {
    border: 0;
    background-color: transparent;
    position: absolute;
    right: 0;
    cursor: pointer;
  }
  main {
    padding-top: 30px;
    margin: 0;
  }
  :global(body) {
    padding: 0;
  }
</style>