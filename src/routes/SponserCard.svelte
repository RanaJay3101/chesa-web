<script>
	export let name;
	export let link;
	export let image;
</script>

<div class="w-full max-w-sm bg-gray-900 border border-gray-900 rounded-lg shadow">
	<a href={link} rel="noreferrer" target="_blank">
		<img class="rounded-t-lg" src={image} alt="" />
	</a>
	<div class="mx-2 my-4">
		<span class="text-3xl font-bold text-white">{name}</span>
	</div>
</div>
