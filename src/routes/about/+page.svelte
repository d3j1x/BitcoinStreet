<script>
	import Adl from "../Adl.svelte";
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="text-column" style="text-align: center;">
	<h1>About <span style="color: #f2a900;font-size: 2rem;">₿itcoin Street</span></h1>

	<p>
		This is a <a href="https://github.com/d3j1x/BitcoinStreet/">opensource</a> app. You can make your own by following the link.
	</p>

	<pre>₿itcoin Street</pre>
<!-- 
	<p>
		The page you're looking at is purely static HTML, with no client-side interactivity needed.
		Because of that, we don't need to load any JavaScript. Try viewing the page's source, or opening
		the devtools network panel and reloading.
	</p> -->

	<p>
		The <a href="/sverdle">Sverdle</a> page illustrates SvelteKit's data loading and form handling. Try
		using it with JavaScript disabled!
	</p>

	
	
</div>

	<div class="pub">
		<Adl />
	</div>

<style>
	h1 {
		font-size: 1rem;
		color: blue;
		font-weight: bolder;
	}

	p {
		font-size: 1.5rem;
		padding: 0.5rem;
	}
</style>