<script>
	
	import logofp from '$lib/freecoins/fp/logofp.png';
	import walletfp from '$lib/freecoins/fp/walletfp.png';
	import cryptofp from '$lib/freecoins/fp/cryptofp.png';


</script>
<svelte:head>
	<title>Free Coins</title>
	<meta name="description" content="TOP - BEST FREE EARNING STEP | FREE CRYPTO COINS | FREE FAUCET | FREE MINING WEBSITE" />
</svelte:head>

<div class="free">
	<h1>BEST OF <br>#FREE EARNING$ <span style="font-size: 1rem; color:#3DFF33;"><br />STEPS</span></h1>
</div>


<div class="text-column">
	
	
	<h2>WALLET</h2>
	<pre>To Store Your #CRYPTO.</pre>

	<div class="fp">

		<span class="logofp">
			<picture>
				<img src={logofp} alt="">
			</picture>
		</span>

	
	

	<p>
		This is a <a href="https://faucetpay.io/?r=5269707">FaucetPay.io</a>
	</p>

	<p>Micropayment Wallet & Earnings Platform</p>

	<img style="max-width: 300px;" src={walletfp} alt="">

	<p>
		You can make your own <a href="https://faucetpay.io/?r=5269707">Wallet</a> by Signup <a href="https://faucetpay.io/?r=5269707"> Register</a> to the Platform.
	</p>
	
	<img src={cryptofp} alt="">

	<h3><a href="https://faucetpay.io/?r=5269707">JOIN NOW</a></h3>
	
	</div>

	

	<!-- <p>
		The page you're looking at is purely static HTML, with no client-side interactivity needed.
		Because of that, we don't need to load any JavaScript. Try viewing the page's source, or opening
		the devtools network panel and reloading.
	</p>

	<p>
		The <a href="/sverdle">Sverdle</a> page illustrates SvelteKit's data loading and form handling. Try
		using it with JavaScript disabled!
	</p> -->
</div>


<style>
	.free{
	margin-top: 10px;
	background-image: linear-gradient(
	to right,
	#462523 0,
    #cb9b51 22%, 
	#f6e27a 45%,
	#f6f2c0 50%,
	#f6e27a 55%,
	#cb9b51 78%,
	#462523 100%
	);
	border: 3px solid gold;
	}

	h1 {
	font-size: 1.5rem;
	text-align: center;
	/* color: #f2a900; */
	color: black;
	font-weight: bolder;
	}

	h2 {
	font-size: 3.5rem;
	font-weight: bolder;
	text-align: center;
	color:blue;
	}
	
	.fp {
		text-align: center;
	}

	.logofp {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
		
		
	}

	.logofp img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}

	/* .fplogo {
		background-position:center;
		background-image: url('../../lib/freecoins/fp/logofp.png');
		background-size:auto;
		min-height: 150px;
		background-repeat: no-repeat;
		border-radius: 20%;
	} */

	pre {
		text-align: center;
		
	}
	p{
		font-size: 1.5rem;
		padding: 1rem 2rem;
	}

	
</style>