<script>
	export let slice;
	import { SliceSimulator } from "@slicemachine/adapter-sveltekit/simulator";

	/** @type {import("@prismicio/client").Content.ImageSlice} */

	
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	
	<article>
		<nav class="navBar">
			<a class="navItem" href="/"><h3>Home</h3></a>
			<a class="navItem" href="/squad-a"><h1>Squad-A</h1></a>
			<a class="navItem" href="/squad-b"><h1>Squad-B</h1></a>
		</nav>
	</article>
</section>

<h1>Members van Squad A</h1>

<section class="student-page">
	{#each slice.items as item}
		<article class="student-card">
			<h2 class="student-name" >{item.name[0].text}</h2>
			<center><img src={item.image.url} alt="" /></center>
			<p class="student-name">Go to my <a href={item.link.url}>Github</a>!</p>
		</article>
	{/each}
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

.navItem:hover {
	transform: scale(1.3);
	transition-duration: 1s;
	color: red;
}

	.student-page {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		flex-direction: row;
		width: 100%;
		gap: 3em;
	}

	.student-name {
		text-align: center;
		align-items: center;
	}
	.student-card {
		
		color: var(--textColor);
		padding: 20px;
		margin: 0 auto;
		margin-bottom:50px;
		border: var(--borderSize);
		border-color: var(--borderColor);
		border-style: solid;
		box-shadow: 10px 15px 20px #ff0000;
		width: 15rem;
		height: 300px;
	}

	article img {
		height: 10em;
		widows: 10em;
	}
</style>
