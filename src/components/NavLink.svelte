<script>
	export let link;
	export let linkText;
</script>

<a
	on:click={() => console.log('rea')}
	href={link}
	class="py-4 px-2  font-semibold hover:text-violet-500 transition duration-300"
	>{linkText}
</a>
