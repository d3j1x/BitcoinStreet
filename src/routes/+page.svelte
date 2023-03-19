<script>


	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';

	import BitcoinPrice from './components/BitcoinPrice.svelte';
	
</script>

<svelte:head>
	<title>Bitcoin Street</title>
	<meta name="description" content="BTC LIVE PRICE $ | Crypto News | Top Free Faucet | Trusted Earnings Website | Mining - Trading - Investing" />
</svelte:head>

<BitcoinPrice />

{#if typeof document !== 'undefined'}
    <script src="//static.surfe.pro/js/net.js"></script>
    <ins class="surfe-be" data-sid="370108"></ins>
    <script>(adsurfebe = window.adsurfebe || []).push({});</script>
{/if}



<section>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		to your new<br />SvelteKit app
	</h1>

	<h2>
		try editing <strong>src/routes/+page.svelte</strong>
	</h2>

	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
