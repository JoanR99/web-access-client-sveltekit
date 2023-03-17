<script lang="ts">
	import Navbar from '../components/Navbar.svelte';
	import '../app.scss';
	import Footer from '../components/Footer.svelte';
</script>

<div class="layout">
	<Navbar />

	<main class="container">
		<slot />
	</main>

	<Footer />
</div>

<style lang="scss">
	.layout {
		display: grid;
		grid-template-rows: auto 1fr auto;
		min-height: 100vh;
	}
</style>
