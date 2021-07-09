<template>
  <div id="app">
          <div v-if="fromBtc == true" id="subPage">
              <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">BTC</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/btc.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromBtc)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(btcname)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
              </div>
          </div>


          <div v-else-if="fromEth == true" >
              <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">ETH</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/eth.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromEth)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(ethname)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
              </div>
          </div>
        
          <div v-else-if="fromLtc == true">
            <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">LTC</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/ltc.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromLtc)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(ltcname)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
              </div>
          </div>

          <div v-else-if="fromXrp == true">
             <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">XRP</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/xrp.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromXrp)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(xrpname)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
              </div>
          </div>

          <div v-else-if="fromDoge == true">
            <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">DOGE</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/doge.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromDoge)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(dogename)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
              </div>
          </div>

          <div v-else-if="fromAda == true">
            <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">ADA</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/ada.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromAda)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(adaname)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
            </div>
          </div>

          <div v-else-if="fromDot == true">
            <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">DOT</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/dot.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromDot)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(dotname)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
            </div>
          </div>

          <div v-else-if="fromBnb == true">
            <div>
                <div id="btcBox"></div>
                <div id="btcTopBox"></div>
                <div id="btcBottomBox"></div>
                <p id="btcSymbol">BNB</p>
                <p id="usdtFont1">USDT</p>
                <h1 id="exchange">Exchange</h1>
                <p id="shitTalk">Trade tokens in an instant</p>
                <img id="btcSwap" src="./assets/bnb.png" width="35" height="35">
                <img id="settings" src="./assets/settings.png" width="35" height="35">
                <img id="clock" src="./assets/clock.png" width="29" height="29">
                <img id="swapArrow" src="./assets/arrow.png" width="60" height="50">
                <img id="usdtSwap1" src="./assets/usdt.png" width="35" height="35">
                <button @click="moveBack(fromBnb)" >Go Back</button>
                <hr id="exchangeLine">
                <input id="btcSwapFrom" size="10" v-on:input="convert(bnbname)" type="text" placeholder="0.0">
                <input id="btcSwapTo" size="10" type="text" placeholder="0.0" readonly>
                <button id="swapButton">Swap</button>
            </div>
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
              <div @click="moveToGoodPage(fromLtc, ltcname)" id="niceArrow3" class="round">
                <div id="cta">
                  <span class="arrow primera next "></span>
                  <span class="arrow segunda next "></span>
                </div>
              </div>
              <div @click="moveToGoodPage(fromXrp, xrpname)" id="niceArrow4" class="round">
                <div id="cta">
                  <span class="arrow primera next "></span>
                  <span class="arrow segunda next "></span>
                </div>
              </div>
              <div @click="moveToGoodPage(fromDoge, dogename)" id="niceArrow5" class="round">
                <div id="cta">
                  <span class="arrow primera next "></span>
                  <span class="arrow segunda next "></span>
                </div>
              </div>
              <div @click="moveToGoodPage(fromAda, adaname)" id="niceArrow6" class="round">
                <div id="cta">
                  <span class="arrow primera next "></span>
                  <span class="arrow segunda next "></span>
                </div>
              </div>
              <div @click="moveToGoodPage(fromDot, dotname)" id="niceArrow7" class="round">
                <div id="cta">
                  <span class="arrow primera next "></span>
                  <span class="arrow segunda next "></span>
                </div>
              </div>
              <div @click="moveToGoodPage(fromBnb, bnbname)" id="niceArrow8" class="round">
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
      ethname: "eth",
      xrpname: "xrp",
      fromXrp: false,
      fromDoge: false,
      dogename: "doge",
      fromAda: false,
      adaname: "ada",
      fromDot: false,
      dotname: "dot",
      fromBnb: false,
      bnbname: "bnb"
    }
  },
  methods: {
    moveToGoodPage(id, nameOfItem){
      if (id == this.fromBtc && nameOfItem == this.btcname){
        this.fromBtc = true
      }
      if (id == this.fromEth && nameOfItem == this.ethname){
        this.fromEth = true;
      }
      if (id == this.fromLtc && nameOfItem == this.ltcname){
        this.fromLtc = true;
      }
      if (id == this.fromXrp && nameOfItem == this.xrpname){
        this.fromXrp = true;
      }
      if (id == this.fromDoge && nameOfItem == this.dogename){
        this.fromDoge = true;
      }
      if (id == this.fromAda && nameOfItem == this.adaname){
        this.fromAda = true;
      }
      if (id == this.fromDot && nameOfItem == this.dotname){
        this.fromDot = true;
      }
      if (id == this.fromBnb && nameOfItem == this.bnbname){
        this.fromBnb = true;
      }
    },
    moveBack(id){
      if (id == this.fromBtc){
        this.fromBtc = false;
      }
      if (id == this.fromEth){
        this.fromEth = false;
      }
      if (id == this.fromLtc){
        this.fromLtc = false;
      }
      if (id == this.fromXrp){
        this.fromXrp = false;
      }
      if (id == this.fromDoge){
        this.fromDoge = false;
      }
      if (id == this.fromAda){
        this.fromAda = false;
      }
      if (id == this.fromDot){
        this.fromDot = false;
      }
      if (id == this.fromBnb){
        this.fromBnb = false;
      }
    },
    toNumberString(num) { 
      if (Number.isInteger(num)) { 
        return num + ".0"
      } else {
      return num.toString(); 
      }
    },
    convert(nameOfCurrency){
      if (nameOfCurrency == this.btcname){
        let a = document.getElementById("btcSwapFrom").value;
        var val = parseFloat(a);
        var ratio = 32000;
        var sol = this.toNumberString(val * ratio);
        document.getElementById("btcSwapTo").value = sol;
      }
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i&subset=devanagari,latin-ext');

#app{
  font-family: 'Poppins', sans-serif;
	font-size: 16px;
	line-height: 24px;
	font-weight: 400;
	color: #14101b;
}
input{
  font-family: 'Poppins', sans-serif;
	font-size: 16px;
	line-height: 24px;
	font-weight: 400;
	color: #14101b;
}
body{
  background-image: linear-gradient(to right, rgba(192, 125, 247, 0.267),rgba(96, 210, 255, 0.333));
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


#btcSwap{
  position: absolute;
  left: 1050px;
  top: 400px;
}
#btcSymbol{
  position: absolute;
  left: 1095px;
  top: 391px;
}
#niceArrowSwapBtc{
  position: absolute;
  left: 900px;
  top: 100px;
}
#usdtSwap1{
  position: absolute;
  left: 1050px;
  top: 565px;
}
#usdtFont1{
  position: absolute;
  left: 1094px;
  top: 554px;
}


#btcBox {
  position: absolute;
  left: 672px;
  width: 370px;
  height: 450px;
  top: 170px;
  border-radius: 30px;
  background-color: white;
  padding: 50px;
  margin: 20px;
}
#btcTopBox {
  position: absolute;
  left: 687px;
  width: 340px;
  height: 10px;
  top: 325px;
  border-radius: 30px;
  background-color: rgb(197, 209, 214);
  padding: 50px;
  margin: 20px;
}
#btcBottomBox {
  position: absolute;
  left: 687px;
  width: 340px;
  height: 10px;
  top: 485px;
  border-radius: 30px;
  background-color: rgb(197, 209, 214);
  padding: 50px;
  margin: 20px;
}

#swapArrow{
  -webkit-transform:rotate(90deg);
  -moz-transform: rotate(90deg);
  -ms-transform: rotate(90deg);
  -o-transform: rotate(90deg);
  transform: rotate(90deg);
  position: absolute;
  left: 900px;
  top: 455px;
 
}
#btcSwapFrom{
  position: absolute;
  left: 730px;
  top: 402px;
  background-color: rgb(197, 209, 214);
  border: none;
}
::placeholder{
  color: #7c8085;
  font-size: 20px;
}
input {
 outline:none;
 font-size: 24px;
}

#btcSwapTo{
  position: absolute;
  left: 730px;
  top: 565px;
  border: none;
  background-color: rgb(197, 209, 214);
}

#exchangeLine{
  position: absolute;
  top: 300px;
  left: 691px;
  background-color: rgb(197, 209, 214);
  width: 469px;
}

#swapButton{
  position: absolute;
  background-color: rgb(89, 203, 252); /* Green */
  border: none;
  color: #ffffff;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  border-radius: 30px;
  font-family: 'Poppins', sans-serif;
  font-size: 20px;
  left: 755px;
  width: 340px;
  height: 60px;
  top: 650px;
}
#swapButton:hover{
  opacity: 0.7;
}

#exchange{
  position: absolute;
  left: 720px;
  font-size: 20px;
  font-weight: 600;
  top: 200px;
}

#shitTalk{
  position: absolute;
  left: 720px;
  color: #7c8085;
  font-size: 15px;
  top: 230px;
}

#settings{
  position: absolute;
  left: 1040px;
  filter: invert(76%) sepia(38%) saturate(1399%) hue-rotate(168deg) brightness(95%) contrast(108%);
  top: 225px;
}
#clock{
  position: absolute;
  left: 1100px;
  filter: invert(76%) sepia(38%) saturate(1399%) hue-rotate(168deg) brightness(95%) contrast(108%);
  top: 228px;
}
</style>
