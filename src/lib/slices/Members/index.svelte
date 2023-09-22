<script>
	export let slice;
	import { SliceSimulator } from "@slicemachine/adapter-sveltekit/simulator";

	/** @type {import("@prismicio/client").Content.ImageSlice} */

	
</script>

<h1>Members van Squad A</h1>

<section>
	{#each slice.items as item}
		<article>
			<h2 class="student-name" >{item.name[0].text}</h2>
			<center><img src={item.image.url} alt="" /></center>
			<p class="student-name">Go to my <a href={item.link.url}>Github</a>!</p>
		</article>
	{/each}
</section>

<style>

	section {
		display: flex;
		flex-direction: column;
		gap: 1em;
	}

	.student-name {
		text-align: center;
		align-items: center;
	}
	article {
		
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
