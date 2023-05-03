<script>
    // @ts-nocheck
    
    import { onDestroy, onMount } from "svelte";
    
    let bitcoinPrice = 0;
    
    onMount(async () => {
      try {
        const response = await fetch('https://api.coindesk.com/v1/bpi/currentprice.json');    
        const data = await response.json();
        bitcoinPrice = data.bpi.USD.rate;
      } catch (error) {
        console.error(error);
      }
    });
    
    let intervalId;
    
    const fetchBitcoinPrice = async () => {
      try {
        const response = await fetch('https://api.coindesk.com/v1/bpi/currentprice.json');
        const data = await response.json();
        bitcoinPrice = data.bpi.USD.rate_float.toFixed(0);
      } catch (error) {
        console.error(error);
      }
    }
    
    intervalId = setInterval(fetchBitcoinPrice, 10000);
    
    onDestroy(() => {
      clearInterval(intervalId);
    });
    
</script>



<span>
  {#if bitcoinPrice}
    ${bitcoinPrice}
  {:else}
  LOADING ...
  {/if}
</span>


<style>
    span {
        color:#3DFF33;
        font-size: 25px;
        background-color: black;
        display: flex;
        justify-content: center;
        align-items: center;
        font-weight: bold;
    }

    @media (min-width: 700px) {
		span {
			/* font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif; */
			font-size: 2rem;
			letter-spacing: 3px;
		}
	}
</style>