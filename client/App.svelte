<script>
	import Navbar from './components/navbar/Navbar.svelte'
	import Footer from './components/footer/Footer.svelte'
</script>

<main>
	<Navbar />
	<Footer />
</main>

<style>
	main {
		text-align: center;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>