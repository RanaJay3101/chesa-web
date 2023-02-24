<script>
	import SponserCard from '../SponserCard.svelte';

	const sponsers = [
		{
			name: 'Google',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		},
		{
			name: 'Google',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		},
		{
			name: 'Google',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		},
		{
			name: 'Google',
			image:
				'https://images.unsplash.com/photo-1677126123251-f269246095f7?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwzfHx8ZW58MHx8fHw%3D&auto=format&fit=crop&w=500&q=60',
			link: 'https://google.com'
		}
	];
</script>

<div class="max-w-[1440px] mx-auto py-8 px-6">
	<h1 class="text-4xl font-black py-4">Sponsers</h1>
	<div class="grid grid-cols-1 md:grid-cols-4 gap-4">
		{#each sponsers as sponser}
			<SponserCard {...sponser} />
		{/each}
	</div>
</div>
