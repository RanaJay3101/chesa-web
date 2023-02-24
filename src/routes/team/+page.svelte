<script>
	import TeamCard from '../TeamCard.svelte';

	const teamMembers = [
		{
			name: 'Raj Patel',
			image:
				'https://images.unsplash.com/photo-1677241817906-a84211b4f627?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxNXx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60',
			linkedIn: '',
			position: 'Developer'
		},
		{
			name: 'Raj Patel',
			image:
				'https://images.unsplash.com/photo-1677241817906-a84211b4f627?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxNXx8fGVufDB8fHx8&auto=format&fit=crop&w=500&q=60',
			linkedIn: '',
			position: 'Developer'
		}
	];
</script>

<div class="max-w-[1440px] mx-auto py-8 px-6">
	<h1 class="text-4xl font-black py-4 underline">Meet our team</h1>
	<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
		{#each teamMembers as member}
			<TeamCard {...member} />
		{/each}
	</div>
</div>
