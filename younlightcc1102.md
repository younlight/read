# 所有商品
<div is="paper-cards" markdown="1">
* ![雨傘](http://rndimg.com/ImageStore/OilPaintingBlue/50x50_OilPaintingBlue_b38ee2f0e0cd41d3b8e2ede12f52fdce.jpg)
  * [雨傘](younlightcc1203)
  * $・120, FREE Shipping to Taiwan
  * 雨傘用來遮蔽雨或陽光日照。使用時，將傘舉在頭上，骨架會撐開布製成的薄膜。用來遮蔽雨的傘稱為雨傘。
* ![掛軸](http://rndimg.com/ImageStore/OilPaintingGreen/50x50_OilPaintingGreen_0ae2164ecee744499c32cb4207b20088.jpg)
  * [掛軸](younlightcc1304)
  * $・120, FREE Shipping to Taiwan
  * 掛軸，又稱立軸，是書畫的一種裝裱形式，是卷軸的一種。先繪畫圖像或書寫文字在紙或絹上，再裝裱成可以懸掛和捲起收納的掛軸。
* ![腳架](http://rndimg.com/ImageStore/OilPaintingRedReal/50x50_OilPaintingRedReal_63433f796d5b4ee7ad0c2caad796c53c.jpg)
  * [腳架](younlightcc1405)
  * $・120, FREE Shipping to Taiwan
  * 腳架，用作增加相機或攝影機穩定性的配件裝備。單腳架通常以重量輕但強度較高的強化鋁合金或碳纖維為其主要材質，以單一腳管配合雲台的設計，減低在使用慢速快門或遠距鏡頭時，因手震引致照片出現模糊。
</div>
<style>button{cursor:pointer;color:aliceblue;background-color:#3f51b5;box-shadow:0 2px 6px 2px rgba(0,0,0,.1);}button[disabled]{cursor:initial;color:grey;background-color:lightgrey;box-shadow:none;}button:active{background-color:#97abda;box-shadow: 0 4px 8px 4px rgba(0,0,0,.1);}</style>
<template id="paper-cards">
<div style="box-shadow: rgba(0, 0, 0, 0.14) 0px 2px 2px 0px, rgba(0, 0, 0, 0.12) 0px 1px 5px 0px, rgba(0, 0, 0, 0.2) 0px 3px 1px -2px;flex: 1 200px;margin: 10px;"><div style="position: relative;height: 100px;"><slot name="bg"><img src="http://rndimg.com/ImageStore/OilPaintingBlue/50x50_OilPaintingBlue_b38ee2f0e0cd41d3b8e2ede12f52fdce.jpg" style="width: 100%;height: 100%;" /></slot><div style="position: absolute;bottom: 0;padding: 5%;font-size: 30px;mix-blend-mode: difference;color: grey;"><slot name="alt">圖說</slot></div></div><div style="padding: 16px;font-size: 14px;"><div style="font-size: 26px;height: 34px;"><slot name="name">品名</slot></div><div style="height: 17px;"><slot name="stars"><svg viewBox="0 0 24 24" preserveAspectRatio="xMidYMid meet" focusable="false" style="pointer-events: none;display: inline-block;height: 100%;margin-right: 3px;"><g><path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#9e9e9e" stroke="#ffc107" stroke-width="0"></path></g></svg></slot></div><p style="font-family: sans-serif;"><slot name="fee">$・Price, Shipping Fee</slot></p><p style="color: #757575;margin: 14px 0;font-size: 16px;"><slot name="desc">說明</slot></p></div><div style="padding: 5px 20px;border-top: 1px solid lightgrey;"><slot name="link"><a><button style="font-size: 16px;padding: 9px 34px;border: none;outline: none;transition: .2s;margin: 5px;">分享</button></a><a><button style="font-size: 16px;padding: 9px 15px;border: none;outline: none;transition: .2s;margin: 5px;">立即購買！</button></a></slot></div></div>
</template>
<script>
customElements.define('paper-cards', class extends HTMLDivElement {constructor() {super(); var ul=this.querySelector('ul'), uls=ul.getElementsByTagName('ul'), papercards=document.all['paper-cards'].content, papercard, lis; function p(s, v) {s=papercard.querySelector('slot[name="'+s+'"]'); if (v) {s.innerHTML=''; s.appendChild(v);} else {return s;}} Array.prototype.forEach.call(uls, ul=>{papercard=papercards.cloneNode(!0); lis=ul.getElementsByTagName('li'); p('bg').firstChild.src=ul.parentNode.firstChild.src; p('alt', document.createTextNode(ul.parentNode.firstChild.alt)); p('name', lis[0].firstChild.firstChild); p('fee', lis[1].firstChild); p('desc', lis[2].firstChild); p('link').lastChild.href=lis[0].firstChild.href; var stars=p('stars'), star=stars.firstChild; stars.appendChild(star.cloneNode(!0)); stars.appendChild(star.cloneNode(!0)); stars.appendChild(star.cloneNode(!0)); stars.appendChild(star.cloneNode(!0)); this.appendChild(papercard);}); this.removeChild(ul);}}, {extends: 'div'});
</script>
