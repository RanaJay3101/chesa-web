<script>
	export let name;
	export let link;
	export let image;
</script>

<div class="w-full max-w-sm border rounded-2xl ">
	<img class="rounded-t-lg" src={image} alt="" />

	<p class="text-3xl font-bold text-center my-4">
		<a href={link} rel="noreferrer" target="_blank">{name}</a>
	</p>
</div>
