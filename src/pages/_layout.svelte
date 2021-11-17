<!-- routify:options preload="proximity" -->
<!-- <nav> is for nav bar -->
<nav>
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
</nav>
<!-- <slot /> is for page content -->
<main>
	<slot />
</main>

<style>
  nav {
    background-color: pink;
    position: fixed;
    height: 30px;
    width: 100%;
  }
  main {
    padding-top: 30px;
    margin: 0;
  }
  :global(body) {
    padding: 0;
  }
</style>