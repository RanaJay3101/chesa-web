<script>
	import EventCard from '../events/eventCard.svelte';
	import TeamCard from './TeamCard.svelte';

	const teamMembers = [
		{
			name: 'Shrey Kaneria',
			image: '/t1.webp',
			position: 'President'
		},
		{
			name: 'Jayvir Atodariya',
			image: '/t2.jpg',
			position: 'Vice President'
		},
		{
			name: 'Manav Agrawal',
			image: '/t3.webp',
			position: 'Treasurer'
		},
		{
			name: 'Meet Shah',
			image: '/t4.webp',
			position: 'General Secretary'
		},
		{
			name: 'Ansh Singh',
			image: '/t5.webp',
			position: 'Organizing Secretary'
		},
		{
			name: 'Aryan Anand',
			image: '/t6.webp',
			position: 'Editor-in-Chief'
		},
		{
			name: 'Rishabh Singh',
			image: '/t7.webp',
			position: 'Technical head'
		},
		{
			name: 'Priyank thakkar',
			image: '/t8.webp',
			position: 'Graphics Head'
		},
		{
			name: 'Sanskar Jain',
			image: '/t9.webp',
			position: 'Sponsorship Head'
		},
		{
			name: 'Khushi Patel',
			image: '/t10.webp',
			position: 'Creative Head'
		},
		{
			name: 'Krishi Prajapati',
			image: '/t11.webp',
			position: 'Creative Head'
		},
		{
			name: 'Romit Patel',
			image: '/t12.webp',
			position: 'Sports Head'
		},
		{
			name: 'Bhargav Patel',
			image: '/t13.webp',
			position: 'Sports Head'
		}
	];

	const faculties = [
		{
			name: 'Dr. Milind Joshipura',
			image: '/millind_joshipura.jpg',
			position: 'Head of the Department'
		},
		{
			name: 'Dr. Narasimha Reddy Ravuru',
			image: '/narasimha_reddy.jpg',
			position: 'Faculty Advisor'
		}
	];
</script>

<section class="text-gray-600 body-font">
	<div class="container px-5 py-24 mx-auto">
		<div class="flex flex-col text-center w-full mb-20">
			<h1 class="text-5xl font-black title-font mb-4 text-gray-900">Guiding Members of the team</h1>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-2 gap-4 justify-items-center">
			{#each faculties as fac}
				<div
					class="py-4 flex flex-col items-center justify-center border rounded-md shadow md:max-w-lg cursor-pointer hover:scale-105 transition-all"
				>
					<img
						class="object-cover sm:w-full rounded-lg md:max-h-96  md:h-auto md:w-60"
						src={fac.image}
						alt={fac.name}
					/>
					<div class="flex flex-col justify-between pt-4 leading-normal">
						<div>
							<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 text-center">
								{fac.name}
							</h5>
							<p class="mb-3 font-semibold text-gray-700 text-center">
								{fac.position}
							</p>
						</div>
					</div>
				</div>
			{/each}
		</div>

		<div class="flex flex-col text-center w-full mb-20 my-10">
			<h1 class="text-5xl font-black title-font mb-4 text-gray-900">Meet our team</h1>
		</div>

		<div class="grid grid-cols-1 md:grid-cols-3 gap-4 items-center ">
			{#each teamMembers as member}
				<TeamCard {...member} />
			{/each}
		</div>
	</div>
</section>
