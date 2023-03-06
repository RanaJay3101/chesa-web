<script>
	let showMenu = false;
	import EventCard from '../routes/events/eventCard.svelte';
	import NavLink from './NavLink.svelte';
	function toggleNavbar() {
		console.log('ran');
		showMenu = !showMenu;
	}

	const navigation = [
		{
			link: '/',
			name: 'Home'
		},
		{
			link: '/events',
			name: 'Events'
		},
		{
			link: '/team',
			name: 'Team'
		},
		{
			link: '/sponsors',
			name: 'Sponsors'
		},
		{
			link: '/contact-us',
			name: 'Contact Us'
		}
	];
</script>

<div>
	<div>
		<nav
			class="container px-6 py-2 mx-auto md:flex md:justify-between md:items-center border-b-[1px] shadow border-gray-300"
		>
			<div class="flex items-center justify-between">
				<div class="flex items-center justify-between">
					<a href="/" class="flex items-center mb-4 sm:mb-0">
						<img src="/l2.png" class="hidden md:block h-12 w-18 mr-3" alt="Nirma" />
						<img src="/l1.png" class="h-20 w-25 mr-3" alt="Logo" />
						<span class="self-center text-2xl font-semibold whitespace-nowrap">ChESA</span>
					</a>
				</div>
				<div on:click={toggleNavbar} class="flex md:hidden">
					<button
						type="button"
						class="text-gray-400 hover:text-gray-900 focus:outline-none focus:text-gray-900"
					>
						<svg
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="3"
							stroke="currentColor"
							class="w-8 h-8"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
							/>
						</svg>
					</button>
				</div>
			</div>

			<!-- Mobile Menu open: "block", Menu closed: "hidden" -->
			<div
				class="flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0 {showMenu
					? 'flex'
					: 'hidden'}"
			>
				{#each navigation as navgationLink}
					<a
						on:click={toggleNavbar}
						href={navgationLink.link}
						class="py-4 px-2  font-semibold hover:text-violet-500 transition duration-300"
						>{navgationLink.name}
					</a>
				{/each}
			</div>
		</nav>
	</div>
</div>
