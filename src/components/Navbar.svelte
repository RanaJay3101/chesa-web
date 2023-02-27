<!-- <script>
	import NavLink from './NavLink.svelte';

	let btn;
	let menu;

	let isOpen = false;

	$: if (btn && menu) {
		btn.addEventListener('click', () => {
			menu.classList.toggle('hidden');
		});
	}
</script>

<nav class="max-w-[1440px] mx-auto border-b-[1px]">
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
						<span class="font-semibold  text-lg">ChESA</span>
					</span>
				</div>

				<div class="hidden md:flex items-center space-x-1">
					<NavLink link="/" linkText="Home" />
					<NavLink link="/events" linkText="Event" />
					<NavLink link="/team" linkText="Team" />
					<NavLink link="/sponsers" linkText="Sponsers" />
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
	<div bind:this={menu} class="hidden transition-all duration-75 mobile-menu">
		<ul class="">
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/" linkText="Home" />
			</li>
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/about" linkText="About" />
			</li>
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/events" linkText="Event" />
			</li>
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/team" linkText="Team" />
			</li>
			<li class="active px-2 py-4 hover:bg-green-50 cursor-pointer">
				<NavLink link="/sponsers" linkText="Sponsers" />
			</li>
		</ul>
	</div>
</nav>

<!-- <nav class="relative bg-white shadow dark:bg-gray-800">
	<div class="container px-6 py-4 mx-auto md:flex md:justify-between md:items-center">
		<div class="flex items-center justify-between">
			<a href="/">
				<img class="w-auto h-6 sm:h-7" src="https://merakiui.com/images/full-logo.svg" alt="" />
			</a>
			<div class="flex lg:hidden">
				<button
					x-cloak
					on:click={() => (isOpen = !isOpen)}
					type="button"
					class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400"
					aria-label="toggle menu"
				>
					<svg
						x-show={!isOpen}
						xmlns="http://www.w3.org/2000/svg"
						class="w-6 h-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M4 8h16M4 16h16" />
					</svg>

					<svg
						x-show={isOpen}
						xmlns="http://www.w3.org/2000/svg"
						class="w-6 h-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
					</svg>
				</button>
			</div>
		</div>

		<div
			x-cloak
			class:menu={isOpen}
			class="absolute inset-x-0 z-20 w-full px-6 py-4 transition-all duration-300 ease-in-out bg-white dark:bg-gray-800 md:mt-0 md:p-0 md:top-0 md:relative md:bg-transparent md:w-auto md:opacity-100 md:translate-x-0 md:flex md:items-center"
		>
			<div class="flex flex-col md:flex-row md:mx-6">
				<a
					class="my-2 text-gray-700 transition-colors duration-300 transform dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-4 md:my-0"
					href="#">Home</a
				>
				<a
					class="my-2 text-gray-700 transition-colors duration-300 transform dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-4 md:my-0"
					href="#">Shop</a
				>
				<a
					class="my-2 text-gray-700 transition-colors duration-300 transform dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-4 md:my-0"
					href="#">Contact</a
				>
				<a
					class="my-2 text-gray-700 transition-colors duration-300 transform dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-4 md:my-0"
					href="#">About</a
				>
			</div>

			<div class="flex justify-center md:block">
				<a
					class="relative text-gray-700 transition-colors duration-300 transform dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-300"
					href="#"
				>
					<svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path
							d="M3 3H5L5.4 5M7 13H17L21 5H5.4M7 13L5.4 5M7 13L4.70711 15.2929C4.07714 15.9229 4.52331 17 5.41421 17H17M17 17C15.8954 17 15 17.8954 15 19C15 20.1046 15.8954 21 17 21C18.1046 21 19 20.1046 19 19C19 17.8954 18.1046 17 17 17ZM9 19C9 20.1046 8.10457 21 7 21C5.89543 21 5 20.1046 5 19C5 17.8954 5.89543 17 7 17C8.10457 17 9 17.8954 9 19Z"
							stroke="currentColor"
							stroke-width="2"
							stroke-linecap="round"
							stroke-linejoin="round"
						/>
					</svg>

					<span class="absolute top-0 left-0 p-1 text-xs text-white bg-blue-500 rounded-full" />
				</a>
			</div>
		</div>
	</div>
</nav>

<style>
	.menu {
		@apply translate-x-0 opacity-100;
	}
</style> -->
<script>
	let showMenu = false;
	import NavLink from './NavLink.svelte';
	function toggleNavbar() {
		showMenu = !showMenu;
	}
</script>

<div>
	<div>
		<nav class="container px-6 py-4 mx-auto md:flex md:justify-between md:items-center border-b-2">
			<div class="flex items-center justify-between">
				<div class="flex items-center justify-between">
					
					<a href="/" class="flex items-center mb-4 sm:mb-0">
						<img
							src="l1.png"
							class="h-20 w-18 mr-3"
							alt="Logo"
						/>
						<span class="font-semibold  text-lg">ChESA</span>
					</a>

					<!-- <a href="/" class="flex items-center mb-4 sm:mb-0 pl-40">
						<img
							src="l2.png"
							class="h-12 mr-3"
							alt="Logo"
						/>
						<span class="font-semibold  text-lg">ChESA</span>
					</a> -->
					
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
				<NavLink link="/" linkText="Home" />
				<NavLink link="/events" linkText="Event" />
				<NavLink link="/team" linkText="Team" />
				<NavLink link="/sponsers" linkText="Sponsers" />
				<NavLink link="/ContactUs" linkText="Contact Us" />
			</div>
		</nav>
	</div>
</div>
