<script>
	import '../app.css';
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';
</script>

<Navbar />
<main class="min-h-screen justify-between">
	<slot />
</main>
<Footer />
