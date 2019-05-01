# 購物車
<div id="flame" markdown="1">
|項目|數量|單價|總價|運費||
|-|-|-|-|-|-|
||<input type="number" min="1" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; text-align: centor;" onchange="localStorage.setItem('cart', localStorage.getItem('cart').split('\n').map(el=>{if (el.indexOf(this.getAttribute('data-id'))>-1) {return el.replace(/,\d+,/, ','+this.value+',');} else {return el;}}).join('\n'));">||||<button>X</button>|

</div>
<script>
(function() {var tbody=document.all.flame.querySelector('table').tBodies[0], button=tbody.querySelector('button').outerHTML, input=tbody.querySelector('input').outerHTML; tbody.innerHTML=''; (localStorage.getItem('cart')||'').split('\n').forEach(function(el) {el=el.split(','); if (el.length==3) {fetch(el[2]+'.csv').then(v=>v.text()).then(v=>{v=v.split(','); tbody.innerHTML+='<tr><td>'+[v[3]?el[0]+'<br><small>'+v[3]+'</small>':el[0]+'<td style="position: relative;">'+input.slice(0, -1)+' value="'+el[1]+'" data-id="'+el[2]+'">', v[0], v[2]?Function('n, p', 'return '+v[2])(el[1], v[0]):el[1]*v[0], v[1], button].join('<td>');});}});})();
</script>
