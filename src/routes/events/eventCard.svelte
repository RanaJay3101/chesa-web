<script>
	export let name;
	export let slug;
	export let link;
	export let image;
	export let description;
	export let category;
</script>

<div class="lg:w-1/2 sm:w-1/2 md:p-4 my-4 px-4 ">
	<div class="flex relative gap-4 min-h-[350px] min-w-full">
		<img
			alt="gallery"
			class="absolute inset-0 w-60 h-80 object-cover object-center"
			src={image}
		/>
		<div
			class="px-8 py-10 relative z-10 w-full border-4 border-gray-200 bg-white opacity-0 transition-all hover:opacity-100 flex flex-col justify-between"
		>
			<div>
				<h2 class="uppercase tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">
					{category}
				</h2>
				<h1 class="font-bold text-2xl title-font text-gray-900 mb-3">{name}</h1>
				<p class="leading-relaxed max-w-md">
					{description}
				</p>
			</div>
			<div class="flex gap-4">
				<a href={'/events/' + slug} class="text-orange-300 inline">View</a>
				<a href={link} class="text-orange-300 inline">Register</a>
			</div>
		</div>
	</div>
</div>
