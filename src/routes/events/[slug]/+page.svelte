<script>
	import { page } from '$app/stores';
	import data from '../data';

	const availablePages = data.map((d) => d.slug);

	const isavailable = availablePages.includes($page.params.slug);
	let event;
	if (isavailable) {
		event = data.filter((d) => d.slug === $page.params.slug)[0];
	}
</script>

{#if isavailable}
	<section class="text-gray-600 body-font">
		<div class="container mx-auto flex flex-col px-5 py-24 justify-center items-center">
			<img class="lg:w-3/6 mb-10 object-cover object-center rounded" src={event.image} alt="hero" />
			<div class="w-full md:w-2/3 flex flex-col mb-16 items-center text-center">
				<h1 class="font-bold text-3xl mb-4 text-gray-900">{event.name}</h1>
				<p class="mb-8 leading-relaxed">
					{event.description}
				</p>
				<div class="flex w-full justify-center items-end">
					<a
						href={event.link}
						class="inline-flex text-white bg-orange-500 border-0 py-2 px-6 focus:outline-none hover:bg-orange-600 rounded text-lg"
					>
						Register</a
					>
				</div>
			</div>
		</div>
	</section>
{:else}
	<div class="h-screen w-full flex flex-col justify-center items-center bg-[#1A2238]">
		<h1 class="text-9xl font-extrabold text-white tracking-widest">404</h1>
		<div class="bg-[#FF6A3D] px-2 text-sm rounded rotate-12 absolute">Page Not Found</div>
		<button class="mt-5">
			<p
				class="relative inline-block text-sm font-medium text-[#FF6A3D] group active:text-orange-500 focus:outline-none focus:ring"
			>
				<span
					class="absolute inset-0 transition-transform translate-x-0.5 translate-y-0.5 bg-[#FF6A3D] group-hover:translate-y-0 group-hover:translate-x-0"
				/>

				<span class="relative block px-8 py-3 bg-[#1A2238] border border-current">
					<a href="/" class="font-black">Go Home</a>
				</span>
			</p>
		</button>
	</div>{/if}
