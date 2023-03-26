<script>
<<<<<<< HEAD
	import Header from '../components/Header.svelte';
=======
	import Header from './Header.svelte';
>>>>>>> 53397c0b8748ce8abc365c0b420f89c00211a21a
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
<<<<<<< HEAD
		<p>visit <a href="#">educa.us</a> to apply for your Visa</p>
=======
		<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
>>>>>>> 53397c0b8748ce8abc365c0b420f89c00211a21a
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
<<<<<<< HEAD
		width: 100%;
=======
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
>>>>>>> 53397c0b8748ce8abc365c0b420f89c00211a21a
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
