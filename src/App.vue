<template>
  <div>
    <body>
          <div v-if="fromBtc == true">
              <img id="btcSwap" src="./assets/btc.png" width="50" height="50">
              <img id="usdtSwap1" src="./assets/usdt.png" width="50" height="50">
              <div id="niceArrowSwapBtc" class="round">
                <div id="cta">
                  <span class="arrow primera next "></span>
                  <span class="arrow segunda next "></span>
                </div>
              </div>

              <input type="text">
              <input type="text" readonly>
              <button>Swap</button>
              <button @click="moveBack(fromBtc)" >Go Back</button>
          </div>
          <div v-else-if="fromEth == true">
              <img id="ethSwap" src="./assets/eth.png" width="50" height="50">
              <img id="usdtSwap2" src="./assets/usdt.png" width="50" height="50">
              <div id="niceArrowSwapEth" class="round">
                <div id="cta">
                  <span class="arrow primera next "></span>
                  <span class="arrow segunda next "></span>
                </div>
              </div>

              <input type="text">
              <input type="text" readonly>
              <button>Swap</button>
              <button @click="moveBack(fromEth)" >Go Back</button>
          </div>
          <div v-else>
            <div @click="moveToGoodPage(fromBtc, btcname)" id="niceArrow" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            <div @click="moveToGoodPage(fromEth, ethname)" id="niceArrow2" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            <div id="niceArrow3" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            <div id="niceArrow4" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            <div id="niceArrow5" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            <div id="niceArrow6" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            <div id="niceArrow7" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            <div id="niceArrow8" class="round">
              <div id="cta">
                <span class="arrow primera next "></span>
                <span class="arrow segunda next "></span>
              </div>
            </div>
            

              <div id="currencies">
                <div id="allUSDT">
                  <img id="usdt" src="./assets/usdt.png" width="50" height="50">
                  <img id="usdt2" src="./assets/usdt.png" width="50" height="50">
                  <img id="usdt3" src="./assets/usdt.png" width="50" height="50">
                  <img id="usdt4" src="./assets/usdt.png" width="50" height="50">
                  <img id="usdt5" src="./assets/usdt.png" width="50" height="50">
                  <img id="usdt6" src="./assets/usdt.png" width="50" height="50">
                  <img id="usdt7" src="./assets/usdt.png" width="50" height="50">
                  <img id="usdt8" src="./assets/usdt.png" width="50" height="50">
                </div>
                <img id="btc" src="./assets/btc.png" width="50" height="50">
                <img id="eth" src="./assets/eth.png" width="50" height="50">
                <img id="ltc" src="./assets/ltc.png" width="50" height="50">
                <img id="xrp" src="./assets/xrp.png" width="50" height="50">
                <img id="doge" src="./assets/doge.png" width="50" height="50">
                <img id="ada" src="./assets/ada.png" width="50" height="50">
                <img id="dot" src="./assets/dot.png" width="50" height="50">
                <img id="bnb" src="./assets/bnb.png" width="50" height="50">
              </div>
          </div>
    </body>
  </div>
</template>

<script>

export default {
  data(){
    return{
      fromBtc: false,
      btcname: "btc",
      fromLtc: false,
      ltcname: "ltc",
      fromEth: false,
      ethname: "eth"
    }
  },
  methods: {
    moveToGoodPage(id, nameOfItem){
      console.log(id);
      if (id == this.fromBtc && nameOfItem == this.btcname){
        this.fromBtc = true
      }
      else if (id == this.fromEth && nameOfItem == this.ethname){
        this.fromEth = true;
      }
    },
    moveBack(id){
      if (id == this.fromBtc){
        this.fromBtc = false
      }
      else if (id == this.fromEth){
        this.fromEth = false
      }
    }
  }
}
</script>

<style>

body {
  background-color: black;
}

#btc:hover{
  opacity: 0.7;
}

#btc{
  position: absolute;
  left: 800px;
  top: 98px;
}


#usdt:hover{
  opacity: 0.7;
}

#usdt{
  position: absolute;
  left: 998px;
  top: 99px;
  
}

#eth:hover{
  opacity: 0.7;
}

#eth{
  position: absolute;
  left: 800px;
  top: 200px;
}

#usdt2{
  position: absolute;
  left: 998px;
  top: 200px;
}

#usdt2:hover{
  opacity: 0.7;
}

#niceArrow2{
  position: absolute;
  left: 900px;
  top: 200px;
}

#ltc:hover{
  opacity: 0.7;
}

#ltc{
  position: absolute;
  left: 800px;
  top: 300px;
}

#usdt3{
  position: absolute;
  left: 998px;
  top: 300px;
}
#usdt3:hover{
  opacity: 0.7;
}
#niceArrow3{
  position: absolute;
  left: 900px;
  top: 300px;
}
#xrp:hover{
  opacity: 0.7;
}

#xrp{
  position: absolute;
  left: 800px;
  top: 400px;
}

#usdt4{
  position: absolute;
  left: 998px;
  top: 400px;
}
#usdt4:hover{
  opacity: 0.7;
}
#niceArrow4{
  position: absolute;
  left: 900px;
  top: 400px;
}

#doge:hover{
  opacity: 0.7;
}

#doge{
  position: absolute;
  left: 800px;
  top: 500px;
}

#usdt5{
  position: absolute;
  left: 998px;
  top: 500px;
}

#usdt5:hover{
  opacity: 0.7;
}

#niceArrow5{
  position: absolute;
  left: 900px;
  top: 500px;
}

#ada:hover{
  opacity: 0.7;
}

#ada{
  position: absolute;
  left: 800px;
  top:  600px;
}

#usdt6{
  position: absolute;
  left: 998px;
  top: 600px;
}
#usdt6:hover{
  opacity: 0.7;
}

#niceArrow6{
  position: absolute;
  left: 900px;
  top: 600px;
}

#dot:hover{
  opacity: 0.7;
}

#dot{
  position: absolute;
  left: 800px;
  top: 700px;
}

#usdt7{
  position: absolute;
  left: 998px;
  top: 700px;
}
#usdt7:hover{
  opacity: 0.7;
}

#niceArrow7{
  position: absolute;
  left: 900px;
  top: 700px;
}

#bnb:hover{
  opacity: 0.7;
}

#bnb{
  position: absolute;
  left: 800px;
  top: 800px;
}

#usdt8{
  position: absolute;
  left: 998px;
  top: 800px;
}

#usdt8:hover{
  opacity: 0.7;
}

#niceArrow8{
  position: absolute;
  left: 900px;
  top: 800px;
}

.center-con {
    display: flex;
    height: 100vh;
    align-items: center;
    justify-content: center;
}



.round {
    position: absolute;
    border: 2px solid #fff;
    width: 40px;
    height: 40px;
    border-radius: 100%;
    
}

#cta{
    width:100%; cursor: pointer; position: absolute;
}

#cta .arrow{left: 30%;}
.arrow {position: absolute; bottom: 0;  margin-left:0px; width: 12px; height: 12px; background-size: contain; top:15px;}
.segunda{margin-left: 8px;}
.next {
	background-image: url(data:image/svg+xml;base64,PHN2ZyBpZD0iTGF5ZXJfMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB2aWV3Qm94PSIwIDAgNTEyIDUxMiI+PHN0eWxlPi5zdDB7ZmlsbDojZmZmfTwvc3R5bGU+PHBhdGggY2xhc3M9InN0MCIgZD0iTTMxOS4xIDIxN2MyMC4yIDIwLjIgMTkuOSA1My4yLS42IDczLjdzLTUzLjUgMjAuOC03My43LjZsLTE5MC0xOTBjLTIwLjEtMjAuMi0xOS44LTUzLjIuNy03My43UzEwOSA2LjggMTI5LjEgMjdsMTkwIDE5MHoiLz48cGF0aCBjbGFzcz0ic3QwIiBkPSJNMzE5LjEgMjkwLjVjMjAuMi0yMC4yIDE5LjktNTMuMi0uNi03My43cy01My41LTIwLjgtNzMuNy0uNmwtMTkwIDE5MGMtMjAuMiAyMC4yLTE5LjkgNTMuMi42IDczLjdzNTMuNSAyMC44IDczLjcuNmwxOTAtMTkweiIvPjwvc3ZnPg==);
}

@keyframes bounceAlpha {
  0% {opacity: 1; transform: translateX(0px) scale(1);}
  25%{opacity: 0; transform:translateX(10px) scale(0.9);}
  26%{opacity: 0; transform:translateX(-10px) scale(0.9);}
  55% {opacity: 1; transform: translateX(0px) scale(1);}
}

.bounceAlpha {
    animation-name: bounceAlpha;
    animation-duration:1.4s;
    animation-iteration-count:infinite;
    animation-timing-function:linear;
}

.arrow.primera.bounceAlpha {
    animation-name: bounceAlpha;
    animation-duration:1.4s;
    animation-delay:0.2s;
    animation-iteration-count:infinite;
    animation-timing-function:linear;
}

.round:hover .arrow{
    animation-name: bounceAlpha;
    animation-duration:1.4s;
    animation-iteration-count:infinite;
    animation-timing-function:linear;
}
.round:hover .arrow.primera{
    animation-name: bounceAlpha;
    animation-duration:1.4s;
    animation-delay:0.2s;
    animation-iteration-count:infinite;
    animation-timing-function:linear;
}

#niceArrow{
  position: absolute;
  left: 900px;
  top: 100px;
}
</style>
