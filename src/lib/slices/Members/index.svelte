<script>
	export let slice;
	import { SliceSimulator } from "@slicemachine/adapter-sveltekit/simulator";

	/** @type {import("@prismicio/client").Content.ImageSlice} */

	console.log(slice);
</script>

<h1>Members van Squad A</h1>

<section>
	{#each slice.items as item}
		<article>
			<h2>{item.name[0].text}</h2>
			<img src={item.image.url} alt="" />
			<p>Go to my <a href={item.link.url}>Github</a>!</p>
		</article>
	{/each}
</section>

<style>
	section {
		flex-direction: column;
		display: flex;
		gap: 1em;
	}

	article {
		text-align: center;
		background-color: pink;
		width: 16em;
		height: 100%;
		padding: 5px;
		border: 4px solid grey;
	}

	article img {
		height: 10em;
		widows: 10em;
	}
</style>
