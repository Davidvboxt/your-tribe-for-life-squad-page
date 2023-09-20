<script>
	/** @type {import("@prismicio/client").Content.WelkomSlice} */
	export let slice;

	console.log(slice)
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	
	<img src={slice.items[0].squadimage.url} alt="">
	
	<a href={slice.items[0].squadlink.url}>Squad A</a>

	<p>{slice.items[0].squadname}</p>
	<img src={slice.items[1].squadimage.url} alt="">
	<p>{slice.items[1].squadname}</p>
	

</section>
