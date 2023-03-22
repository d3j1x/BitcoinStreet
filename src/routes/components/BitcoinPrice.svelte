
<script>
// @ts-nocheck

  import { onMount } from 'svelte';

  let satoshi = 1000;
  let usd = 0;

  const fetchPrice = async () => {
    const response = await fetch('https://api.coindesk.com/v1/bpi/currentprice.json');
    const data = await response.json();
    const rate = data.bpi.USD.rate_float;
    usd = (satoshi * rate / 100000000).toFixed(3);
  };

  onMount(fetchPrice);

  function handleInput(event) {
    satoshi = event.target.value;
    fetchPrice();
  }
</script>


<div class="bitcoin-price">
    <h3><span style="color: #f2a900;">BTC:</span> Satoshi To USD</h3>
    <input class="bitcoin-price__input" type="number" bind:value={satoshi} on:input={handleInput} placeholder="Enter Satoshi amount" />
    <p class="bitcoin-price__output">Price: ${usd}</p>
</div>

<style>
    .bitcoin-price {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 1rem;
      margin-bottom: 1rem;
      border: 5px solid  #d3d3d3;
      border-radius: 8px;
      background: rgba(0, 0, 0, 0.8);
    }
  
    .bitcoin-price__input {
      padding: 0.5rem;
      font-size: 1.2rem;
      font-weight: bold;
      border: 2px solid #1c1c1e;
      border-radius: 8px;
      text-align: center;
      width: 80%;
      max-width: 400px;
      margin: 0.5rem;
      background:goldenrod;
      
      
    }
  
    .bitcoin-price__input:focus {
      outline: none;
      width: 92%;
      border-color: #0077ff;
      box-shadow: 0 0 0 3px rgba(0, 119, 255, 0.3);
    }
  
    .bitcoin-price__output {
      font-size: 1.5rem;
      font-weight: bold;
      color: #3DFF33;
      
    }
  </style>