<script>
	import { page } from '$app/stores';
	import { goto } from '$app/navigation';
	import { onMount } from 'svelte';

	// import logo from '$lib/images/svelte-logo.svg';
	import logo from '$lib/images/logo.png';
	import logopen from '$lib/images/logopen.png';
	// import github from '$lib/images/github.svg';

	import LivePrice from './components/LivePrice.svelte';
	
	

  	let isSticky = false;

  	function handleScroll() {
    isSticky = window.pageYOffset > 0;
  	}

  	onMount(() => {
    window.addEventListener('scroll', handleScroll);
    return () => {
      window.removeEventListener('scroll', handleScroll);
    };
  	});

	
	function refreshPage() {
    	setTimeout(() => {
    	  location.reload();
    	}, 250);
  	}

 	function handleClick() {
    	goto('/');
    	refreshPage();
 	}

</script>


<div class:sticky={isSticky} style="z-index: 10;">
	<!-- Your component content here -->

	<LivePrice />
	
	<header>
		<!-- <div class="corner">
			<a href="https://kit.svelte.dev">
				<img src={logo} alt="SvelteKit" />
			</a>
		</div> -->
	
		<div class="corner logo-container">
			<a href="{$page.url.pathname}">
				<img src={logo} alt="BtcStreet" />
			</a>
		</div>
		
	
		<nav>
			<svg viewBox="0 0 2 3" aria-hidden="true">
				<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
			</svg>
			<ul>
				<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					<a href="/" on:click|preventDefault={handleClick}>STREET</a>
				</li>
	
				<li aria-current={$page.url.pathname.startsWith('/freecoins') ? 'page' : undefined}>
					<a href="/freecoins">FreeCoins</a>
				</li>
				
				<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
					<a href="/about">About</a>
				</li>
				
			</ul>
			<svg viewBox="0 0 2 3" aria-hidden="true">
				<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
			</svg>
		</nav>
	
		<!-- <div class="corner">
			<a href="https://github.com/sveltejs/kit">
				<img src={github} alt="GitHub" />
			</a>
		</div> -->
		<div class="corner">
			<a href="https://github.com/d3j1x/BitcoinStreet/">
				<img src={logopen} alt="OpenSource" />
			</a>
		</div>
	</header>

</div>




<style>


 	.sticky {
    	position: sticky;
    	top: 0;
    	/* background-color: #006400; */
    	/* padding: 10px; */
    	/* border-bottom: 5px solid #006400; */
  	}


	header {
		display: flex;
		justify-content: space-between;
		background-color: black;
		border-bottom: 5px solid black;
	}

	

	.corner {
		width: 3em;
		height: 3em;
	}

	.logo-container {
  /* display: inline-block; */
  position: relative;
  /* width: 100px;
  height: 100px; */
  
}

.logo-container img {
  position: absolute;
  /* top: 0;
  left: 0; */
  animation: spin 2s linear infinite;
}

@keyframes spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}


	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		/* --background: rgba(255, 255, 255, 0.7); */
		--background: rgba(255, 255, 255, 0.2);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 10px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		/* border-top: var(--size) solid var(--color-theme-1); */
		border-top: var(--size) solid #3DFF33;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		/* color: var(--color-text); */
		color: white;
		font-weight: 800;
		/* font-size: 0.8rem; */
		font-size: 0.9rem;
		/* text-transform: uppercase; */
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		/* color: var(--color-theme-1); */
		color: blue;
	}
</style>
