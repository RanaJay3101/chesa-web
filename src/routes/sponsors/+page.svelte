<script>
	import SponserCard from './SponserCard.svelte';

	const sponsers = [
		
		{
			name: 'Shree Hari Education Consultant Pvt. Ltd. ',
			image:'/shreehari.png',
			link: 'https://shreehari.in/'
		},

		{
			name: 'Polo Safari',
			image:'/polosafari.png',
			link: '/sponsors'
		},
		{
			name: 'Engenius Gate Academy',
			image:'/engenius.png',
			link: '/sponsors'
		},
		{
			name: '1920 Tatooe Hub',
			image:'/tatoohub.png',
			link: '/sponsors'
		},
		{
			name: 'Delhi Institute of Civil Services ',
			image:'/dics.png',
			link: '/sponsors'
		}
		
	];
</script>

<section class="text-gray-600 body-font">
	<div class="container px-5 py-24 mx-auto">
		<div class="flex flex-col text-center w-full mb-20">
			<h1 class="text-5xl font-black title-font mb-4 text-gray-900">Sponsors</h1>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-4">
			{#each sponsers as sponser}
				<SponserCard {...sponser} />
			{/each}
		</div>
	</div>
</section>
