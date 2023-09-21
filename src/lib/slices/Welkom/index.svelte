<script>
	/** @type {import("@prismicio/client").Content.WelkomSlice} */
	export let slice;

	console.log(slice)
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	
	<article class="allSquads">

		<article class="squadA">
			<img src={slice.items[0].squadimage.url} alt="">
			<h1 class="squadNameA">{slice.items[0].squadname}</h1>
		</article>

		<article class="squadB">
			<img src={slice.items[1].squadimage.url} alt="">
			<h1 class="squadNameB">{slice.items[1].squadname}</h1>
		</article>
		
	</article>

</section>


<style>
	
:root{
	--textColor: white;
	--backgroundColor: black;
	--borderColor: red;
	--borderSize: 5px;
}

.allSquads{
	display: flex;
	background-color: var(--backgroundColor);
}

.squadA{
	color: var(--textColor);
	padding: 20px;
	margin: 0 auto;
	margin-bottom:50px;
	border: var(--borderSize);
	border-color: var(--borderColor);
	border-style: solid;
}
.squadNameA{
	text-align: center;
	font-size: 36px;
}

.squadB{
	color: var(--textColor);
	margin-top: 50px;
	margin: 0 auto;
	border: var(--borderSize);
	border-color: var(--borderColor);
	border-style: solid;
}

.squadNameB{
	text-align: center;
	font-size: 36px;
}





.squadA:hover{
  animation-name: scale;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}

.squadB:hover{
  animation-name: scale;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}
@keyframes scale {
0%{
  scale: 1;
}
50%{
  scale: 1.1;
}
100% {
    scale: 1;
  }
}


@media (max-width: 700px){
  .allSquads{
      display: flex;
      flex-direction: column;
      
  }
}

</style>