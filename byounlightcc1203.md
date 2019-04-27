# 購物車
<div id="flame" markdown="1">
|項目|數量|單價|總價|運費||
|-|-|-|-|-|-|
||||||<button>X</button>|

</div>
<script>
(function() {var tbody=document.all.flame.querySelector('table').tBodies[0], button=tbody.querySelector('button').outerHTML; tbody.innerHTML=''; (localStorage.getItem('cart')||'').split('\n').forEach(function(el) {el=el.split(','); if (el.length==3) {fetch(el[2]+'.csv').then(v=>v.text()).then(v=>{v=v.split(','); tbody.innerHTML+='<tr>'+['', v[3]?el[0]+'<small>'+v[3]+'</small>':el[0], el[1], v[0], v[2]?Function('n, p', 'return '+(v[2][0]=='"'?(v[2].match(/^"(.*)"$/)||[])[1]:v[2]))(v[0], el[1]):v[0]*el[1], v[1], button].join('<td>');});}});})();
</script>
