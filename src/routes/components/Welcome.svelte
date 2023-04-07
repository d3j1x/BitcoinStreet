
<div class="loader">
    <h2>WELCOME</h2>
</div>


<style>
    .loader
{
    position: relative;
    padding:0;
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
    color: gold;
    letter-spacing: 5px;
    font-size: 2.5em;
    font-weight:bold;
    text-transform: uppercase;
    animation: typing 8s steps(9) infinite;
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
        width:239px;
    }
}
</style>