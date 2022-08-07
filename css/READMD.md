CSS Note
===
- CSS 程式碼是由規則所組成的，包含
	- 選擇器 Selector
	- 宣告 Declaration {}
		- 屬性 Property
		- 值 Value
- `Selector { Property1: Value; Property2: Value}`

# 選擇器 Selectors
1. 標籤選擇器 Tag Selector / Type Selector
	- 以 HTML 標籤為選擇對象，不可使用自訂的名稱
	- 會一概套用所有同類的標籤
	- 若有多種標籤都要套用相同的樣式，可以將其用逗號分隔寫在一起
		- `div, p, a {}`
			- \<div\>、\<p\>、\<a\> 三種標籤的格式就會一起被設定
2. 類別選擇器 Class Selector
	- `.ClassName {}`
	- 將格式設定好後，針對想要套用格式的標籤可以直接設定取用
		- CSS style: `.textred {color: red;}`
			- HTML: `<p class="textred">hello</p>`
			- HTML: `<a href="google.com" class="textred">google</a>`
> `標籤選擇器.類別選擇器 {}` 專屬標籤的類別選擇器
> example: `p.textred {color: red;}`
> 若是以此種方式撰寫格式設定的話，此種 class 就只能套用在 p 這個標籤上，若是要在其他的標籤上套用此類別是不會有反應的
3. 識別碼選擇器 ID Selector
	- `#IdName {}`
	- 與類別選擇器功能相似，只是因為這是以識別碼來進行選擇套用，故為唯一值，在同一 HTML 文檔中不可重複套用使用
	- CSS style: `#textred {color: red;}`
			- HTML: `<p id="textred">hello</p>`