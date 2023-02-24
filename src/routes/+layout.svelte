<script>
	import '../app.css';
	import Footer from './Footer.svelte';
	import Navbar from './Navbar.svelte';
</script>

<main>
	<Navbar />
	<slot />
	<Footer />
</main>
