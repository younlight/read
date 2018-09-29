## 代購單

|物品名稱|網址|數量|金額|<input type="button" value="+" onclick="var tr=document.createElement('tr'); tr.innerHTML='<td><input name=sth></td><td><input name=url></td><td><input value=1 size=1 name=quanity></td><td><input name=subtotal size=1></td><td><input type=button value=X onclick=this.parentNode.parentNode.parentNode.removeChild(this.parentNode.parentNode);></td></tr>'; this.parentNode.parentNode.parentNode.appendChild(tr);">
|-|-|-|-|-
|<input name="">|<input name="">|<input value="1" size="1" name="quanity">|<input size="1" name="subtotal">|<input type="button" value="X" onclick="this.parentNode.parentNode.parentNode.removeChild(this.parentNode.parentNode);">
|總計|||<input size="1" name="total">

### 優惠券（選填）
<div id="optional" style="display: none;"><input name="coupon" type="radio" value="1000-100">滿千折百</div>

### 預計付款金額
<input size="2" name="pay">

### 配送方式
填入宅配地址或7-11店號與店名
<textarea name="transfer"></textarea>

### 電子郵件
送出後將確認訂購內容並回傳匯款帳號，請確認查收電子郵件
<input type="email" name="email">

### 付款方式
