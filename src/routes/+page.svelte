<script>




	// import Counter from './Counter.svelte';
	// import welcome from '$lib/images/svelte-welcome.webp';
	// import welcome_fallback from '$lib/images/svelte-welcome.png';

	import BitcoinPrice from './components/BitcoinPrice.svelte';

	import Ad from './Ad.svelte';


	import Converter from './components/Converter.svelte';

	import Welcome from './components/Welcome.svelte';

	
	
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

	<!-- <div class="loader">
		<h2>WELCOME</h2>
	</div> -->
	<div class="c" >
		<Welcome />

	<h1>
		<!-- <span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span> -->
	
		<span style="color: blue;">TO</span><br /><span style="color: #f2a900;">₿TC </span>STREET<br />❤
	</h1>

	</div>
	
	

	<!-- <h2>
		TO<br />₿TC STREET<br />❤
	</h2> -->

	<!-- <Counter /> --> 
	
</section>


<Converter />










<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
		
	}

	.c {
		border: 2px dotted lawngreen;
		border-radius: 20%; 
		margin:20px 0;
		background:black;
		padding: 0 10px;
	}

	h1 {
		width: 100%;

		font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
		font-size: 2.66rem;
		
	
	}

	/* .welcome {
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
	} */

	/* .loader
{
    position: relative;
}

.loader::before
{
    content: "";
    position: relative;
    top: 0;
    right:0;
    width: 2px;
    height: 100%;
    background: #03e9f4;
    animation: blinkCursor 0.8s step(3) infinite;
}

@keyframes blinkCursor
{
    0%,75%
    {
        opacity: 1;
    }
    76%,100%
    {
        opacity: 0;
    }

}

.loader h2
{
    position: relative;
    color: #03e9f4;
    letter-spacing: 5px;
    font-size: 4em;
    text-transform: uppercase;
    animation: typing 8s steps(10) infinite;
    overflow: hidden;

}

@keyframes typing
{
    0%,90%,100%
    {
        width: 0;
    }
    30%,60%
    {
        width:420.88px;
    }
} */
	
	
	
</style>
