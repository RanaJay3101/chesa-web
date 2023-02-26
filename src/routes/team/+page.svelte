<script>
	import TeamCard from './TeamCard.svelte';

	const teamMembers = [
		{
			name: 'Shrey Kaneria',
			image:
				'/t1.webp',
			position: 'President'
		},
		{
			name: 'Jayvir Atodariya',
			image:
				'/t2.jpg',
			position: 'Vice President'
		},
		{
			name: 'Manav Agrawal',
			image:
				'/t3.webp',
			position: 'Treasurer'
		},
		{
			name: 'Meet Shah',
			image:
				'/t4.webp',
			position: 'General Secretary'
		},
		{
			name: 'Ansh Singh',
			image:
				'/t5.webp',
			position: 'Organizing Secretary'
		},
		{
			name: 'Aryan Anand',
			image:
				'/t6.webp',
			position: 'Editor-in-Chief'
		},
		{
			name: 'Rishabh Singh',
			image:
				'/t7.webp',
			position: 'Technical head'
		},
		{
			name: 'Priyank thakkar',
			image:
				'/t8.webp',
			position: 'Graphics Head'
		},
		{
			name: 'Sanskar Jain',
			image:
				'/t9.webp',
			position: 'Sponsorship Head'
		},
		{
			name: 'Khushi Patel',
			image:
				'/t10.webp',
			position: 'Creative Head'
		},
		{
			name: 'Krishi Prajapati',
			image:
				'/t11.webp',
			position: 'Creative Head'
		},
		{
			name: 'Romit Patel',
			image:
				'/t12.webp',
			position: 'Sports Head'
		},
		{
			name: 'Bhargav Patel',
			image:
				'/t13.webp',
			position: 'Sports Head'
		}
	];
</script>

<div class="max-w-[1440px] mx-auto px-6">
	<h1 class="text-4xl font-black py-8 underline text-center ">Meet our team</h1>
	<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
		{#each teamMembers as member}
			<TeamCard {...member} />
		{/each}
	</div>
</div>
