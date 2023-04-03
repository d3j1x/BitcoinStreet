<script>




	// import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';

	import BitcoinPrice from './components/BitcoinPrice.svelte';

	import Ad from './Ad.svelte';

	import Converter from './components/Converter.svelte';



	
	
</script>

<svelte:head>
	<title>Bitcoin Street</title>
	<meta name="description" content="BTC LIVE PRICE $ | Crypto News | Top Free Faucet | Trusted Earnings Website | Mining - Trading - Investing | Convert Btc Satoshi To USD" />
</svelte:head>

<BitcoinPrice />

<div class="pub">
	<Ad />
</div>


<Converter />



<section>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		TO <br />  ₿TC STREET  <br /> ❤
	</h1>

	

	<!-- <h2>
		<strong>APP</strong>
	</h2>

	<Counter /> -->
	
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
