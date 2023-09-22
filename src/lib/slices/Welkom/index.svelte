<script>
	/** @type {import("@prismicio/client").Content.WelkomSlice} */
	export let slice;

	console.log(slice)
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	

	<h1 class="title">Kies een squad!</h1>

	<article class="allSquads">

		
			<article class="squadA">
				<a class="link" href="/squad-a">
					<img src={slice.items[0].squadimage.url} alt="">
					<h1 class="squadNameA">{slice.items[0].squadname}</h1>
				</a>
			</article>
		

		<article class="squadB">
			<a class="link" href="/squad-b">
				<img src={slice.items[1].squadimage.url} alt="">
				<h1 class="squadNameB">{slice.items[1].squadname}</h1>
			</a>
		</article>
		
	</article>

</section>


<style>
	
:root{
	--textColor: white;
	--backgroundColor: black;
	--borderColor: red;
	--squadBorderColor: white;
	--squadBorderSize: 2px;
	--borderSize: 3px;
}

.title{
	margin-bottom: 30px;
	color: white;
	font-size: 28px;
}

.link{
	text-decoration: none;
	color: white;
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
	box-shadow: 10px 15px 20px #ff0000;
}
.squadNameA{
	text-align: center;
	font-size: 36px;
	padding: 5px;
	border: var(--squadBorderSize);
	border-color: var(--squadBorderColor);
	border-style: solid;
}

.squadB{
	color: var(--textColor);
	margin-top: 50px;
	padding: 20px;
	margin: 0 auto;
	border: var(--borderSize);
	border-color: var(--borderColor);
	border-style: solid;
	box-shadow: 10px 15px 20px #ff0000;
}

.squadNameB{
	text-align: center;
	font-size: 36px;
	padding: 5px;
	border: var(--squadBorderSize);
	border-color: var(--squadBorderColor);
	border-style: solid;
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


@media (max-width: 760px){
  .allSquads{
      display: flex;
      flex-direction: column;
  }
}

@media (min-width: 460px){
  .title{
      margin-left: 40%;
  }
}

</style>