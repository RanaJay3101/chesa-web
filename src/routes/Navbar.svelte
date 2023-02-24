<script>
	import NavLink from '../components/NavLink.svelte';

	let btn;
	let menu;

	$: if (btn && menu) {
		btn.addEventListener('click', () => {
			menu.classList.toggle('hidden');
		});
	}
</script>

<nav class="max-w-[1440px] mx-auto">
	<div class="px-4">
		<div class="flex justify-between">
			<div class="w-full flex justify-between space-x-7">
				<div>
					<span class="flex items-center py-4 px-2 cursor-pointer">
						<img
							src="http://iichemrc.org/wp-content/themes/iichemrc/images/logo.jpg"
							alt="Logo"
							class="h-10 w-18 mr-2"
						/>
						<span class="font-semibold  text-lg">IIChe Nirma</span>
					</span>
				</div>

				<div class="hidden md:flex items-center space-x-1">
					<NavLink link="/" linkText="Home" />
					<NavLink link="/about" linkText="About" />
					<NavLink link="/event" linkText="Event" />
				</div>
			</div>

			<div class="md:hidden flex items-center">
				<button bind:this={btn} class="outline-none mobile-menu-button">
					<svg
						class=" w-6 h-6 text-gray-500 hover:text-green-500 "
						x-show="!showMenu"
						fill="none"
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						viewBox="0 0 24 24"
						stroke="currentColor"
					>
						<path d="M4 6h16M4 12h16M4 18h16" />
					</svg>
				</button>
			</div>
		</div>
	</div>
	<!-- mobile menu -->
	<div bind:this={menu} class="hidden transition-all duration-75 mobile-menu">
		<ul class="">
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/" linkText="Home" />
			</li>
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/about" linkText="About" />
			</li>
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/event" linkText="Event" />
			</li>
		</ul>
	</div>
</nav>
