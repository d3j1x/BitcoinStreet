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
	<meta name="description" content="BTC LIVE PRICE $ | Crypto, Bitcoin News | Crypto Converter | Top Free Faucet | Trusted Earnings Website | Mining - Trading - Investing | Convert Btc Satoshi To USD" />
</svelte:head>

<BitcoinPrice />

<div class="pub">
	<Ad />
</div>

<div style="margin-top: 25px; font-weight:bold">
	<script type="text/javascript" src="https://files.coinmarketcap.com/static/widget/currency.js"></script><div class="coinmarketcap-currency-widget" data-currencyid="1" data-base="USD" data-secondary="" data-ticker="true" data-rank="true" data-marketcap="true" data-volume="true" data-statsticker="true" data-stats="USD"></div>
</div>


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


<Converter />

<div>
	<script src="https://cointelegraph.com/news-widget" data-ct-widget-limit="10" data-ct-widget-theme="dark" data-ct-widget-size="tiny" data-ct-widget-priceindex="true" data-ct-widget-images="true" data-ct-widget-currency="USD" data-ct-widget-category="bitcoin,ethereum" data-ct-widget-language="en"></script>
</div>









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
