<script>
// @ts-nocheck

	import { onDestroy, onMount } from "svelte";
  let bitcoinPrice = 0;
  onMount(async () => {
    const response = await fetch('https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd');
    const data = await response.json();
    bitcoinPrice = data.bitcoin.usd;
  });


  
  let intervalId;

  const fetchBitcoinPrice = async () => {
    try {
      const response = await fetch('https://api.coingecko.com/api/v3/simple/price?ids=bitcoin&vs_currencies=usd');
      const data = await response.json();
      bitcoinPrice = data['bitcoin']['usd'];
    } catch (error) {
      console.error(error);
    }
  }

  intervalId = setInterval(fetchBitcoinPrice, 10000);

  onDestroy(() => {
    clearInterval(intervalId);
  });
</script>


<div id="loading">
    <div class="waviy">
<span style="--i:1">₿</span>
<span style="--i:2">i</span>
<span style="--i:3">t</span>
<span style="--i:4">c</span>
<span style="--i:5">o</span>
<span style="--i:6">i</span>
<span style="--i:7">n</span>
<span style="--i:8">&nbsp;&nbsp;</span>
<span style="--i:9">s</span>
<span style="--i:10">t</span>
<span style="--i:11">r</span>
<span style="--i:12">Ǝ</span>
<span style="--i:13">e</span>
<span style="--i:14">t</span>
</div>
</div>

<span style="color:#3DFF33;font-size: 25px;background-color: black;
display: flex;
justify-content: center;
align-items: center;">
  {#if bitcoinPrice}
    ${bitcoinPrice}
  {:else}
  LOADING ...
  {/if}
</span>




<style>




    #loading {
  background-color: black;
  display: flex;
  justify-content: center;
  align-items: center;
  
  
}
.waviy {
  position: relative;
}
.waviy span {
  position: relative;
  display: inline-block;
  font-size: 23px;
  color: yellow;
  text-transform: uppercase;
  animation: flip 4s infinite;
  animation-delay: calc(.2s * var(--i))
}
@keyframes flip {
  0%,80% {
    transform: rotateY(360deg) 
  }
}
</style>