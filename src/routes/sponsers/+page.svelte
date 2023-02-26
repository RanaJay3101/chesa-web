<script>
	import SponserCard from './SponserCard.svelte';

	const sponsers = [
		{
			name: 'will be announcing ..',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		},
		{
			name: 'will be announcing ..',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		},
		{
			name: 'will be announcing ..',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		},
		{
			name: 'will be announcing ..',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		}
	];
</script>

<section class="text-gray-600 body-font">
	<div class="container px-5 py-24 mx-auto">
		<div class="flex flex-col text-center w-full mb-20">
			<h1 class="text-5xl font-black title-font mb-4 text-gray-900">Sponsers</h1>
			<p class="lg:w-2/3 mx-auto leading-relaxed text-base">
				Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos, laudantium sapiente!
				Sapiente laudantium nobis officiis. Quod earum fugit, ea facere voluptates atque architecto
				sed ad esse ab nemo, nobis nostrum.
			</p>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-4 gap-4">
			{#each sponsers as sponser}
				<SponserCard {...sponser} />
			{/each}
		</div>
	</div>
</section>
