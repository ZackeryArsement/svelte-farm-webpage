<script>
	import Navbar from '../src/components/navbar/Navbar.svelte'
	import Footer from '../src/components/footer/Footer.svelte'
	import Display from './components/display/Display.svelte';
</script>

<main>
	<div class='display'>
		<Display />
	</div>
	<Navbar />
	<Footer />
</main>

<style>
	main {
		text-align: center;
		max-width: 240px;
		margin: 0 auto;
		padding: 0;
	}

	@media (min-width: 320px) {
		main {
			max-width: none;
		}
	}
</style>