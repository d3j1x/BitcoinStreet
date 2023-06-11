

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
<span style="--i:12">e</span>
<span style="--i:13">e</span>
<span style="--i:14">t</span>
  </div>
</div>


<style>

#loading {
  background-color: black;
  /* background-color: rgba(0, 0, 0, 0.8); */
  display: flex;
  justify-content: center;
  align-items: center;
  }

.waviy {
  position: relative;
  font-family: 'Russo One', sans-serif;
  /* font-weight: bold; */
}

.waviy span {
  position: relative;
  display: inline-block;
  font-size: 25px;
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

@media (min-width: 700px) {
    .waviy span {
		
			font-size: 2.5rem;
			letter-spacing: 3px;
		}
	}
</style>