<script>
	/** @type {import("@prismicio/client").Content.NavbarSlice} */
	export let slice;

	console.log(slice)
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	
	<article>
		<nav class="navBar">
			<a class="navItem" href="/"><h3>Home</h3></a>
			<a class="navItem" href="/"><h1>Squad-A</h1></a>
			<a class="navItem" href="/"><h1>Squad-B</h1></a>
		</nav>
	</article>
</section>


<style>
:root{
	background-color: black;
}
.navBar{
	background-color: black;
	display: flex;
	justify-content: space-around;
	border-bottom: 2px;
	border-color: black;
	border-style: solid;
	margin-bottom: 100px;
}

.navItem{
	text-decoration: none;
	color:white;
	
}

.navItem:hover{
  animation-name: scale;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  
  
}

@keyframes scale {
0%{
  scale: 1;
  color: white;
}

100% {
    scale: 1.3;
	color: aqua;
  }

  
}

</style>