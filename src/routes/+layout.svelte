<script>

	import Header from './Header.svelte';
	import Sitename from './Sitename.svelte';
	import './styles.css';

	// const script = document.createElement('script');
    // script.src = '//static.surfe.pro/js/net.js';
    // document.body.appendChild(script);

</script>

<div class="app">

	<Sitename />


	<Header />


	

	<main>
		<slot />
	</main>

	<footer>
		<p>WELCOME TO ₿ITCOIN STREET</p>
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
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
		margin-bottom: 50px;
		
	}

	footer p {

		color: white;
		background: #0077ff;
		font: 1rem sans-serif;
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
