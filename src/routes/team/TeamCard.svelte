<script>
	export let name;
	export let image;
	export let linkedIn;
	export let position;
</script>

<a
	href="/"
	class="flex flex-col items-center bg-gray-50 border rounded-md shadow md:flex-row md:max-w-xl "
>
	<img
		class="object-cover w-full rounded-t-lg h-96 md:h-auto md:w-48 md:rounded-none md:rounded-l-lg"
		src={image}
		alt={name}
	/>
	<div class="flex flex-col justify-between p-4 leading-normal">
		<div>
			<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900">{name}</h5>
			<p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{position}</p>
		</div>
		<div><a href={linkedIn}>Linked in</a></div>
	</div>
</a>
