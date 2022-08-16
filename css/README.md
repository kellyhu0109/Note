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
> `標籤選擇器.類別選擇器 {}` 專屬標籤的類別選擇器 <br>
> example: `p.textred {color: red;}` <br>
> 若是以此種方式撰寫格式設定的話，此種 class 就只能套用在 p 這個標籤上，若是要在其他的標籤上套用此類別是不會有反應的
3. 識別碼選擇器 ID Selector
	- `#IdName {}`
	- 與類別選擇器功能相似，只是因為這是以識別碼來進行選擇套用，故為唯一值，在同一 HTML 文檔中不可重複套用使用
	- CSS style: `#textred {color: red;}`
		- HTML: `<p id="textred">hello</p>`

# 三種套用 CSS 的方式
1. 插在 HTML `<head>...</head>` 中
	- ```html=
	  <head>
		  <style type="text/css">
		  ...
		  </style>
	  </head>
	  ```
	- `<style>` 標籤中的 `type="text/css"` 意思是告訴瀏覽器「直到此標籤結束為止，從下一列開始是用來定義CSS樣式」
2. 直接插在標籤內
	- ```html=
	  <p style="color: red; font-size: 20px">Hello</p>
	  ```
3. 另外寫一個 css 檔，再由 HTML 呼叫引入
	- 有兩種方式，都放在 `<head>...</head>` 中
	- ```html=
	  <!-- 方法一 -->
	  <link rel="stylesheet" type="text/css" href="css檔案位置">

	  <!-- 方法二 -->
	  <style type="text/css">
		  @import url(css檔案位置);
	  </style>
	  ```
	- |  | `<link>` | `@import` |
	  | --- | --- | --- |
	  | 使用範圍 | 為 HTML 語法，故只能在 HTML 網頁中使用 | 為 CSS 語法，可以於網頁中的樣式定義`<style>`中使用，也可用於 css 樣式檔中 |
	  | 瀏覽器載入樣式表時機 | 讀到標籤時不會載入樣式表，直到讀取到使用樣式的標籤時，才會載入樣式檔內容 | 讀到 `@import` 指令就會立刻載入樣式內容 |

# CSS 相關屬性設定
## margin
在區塊內四周設定留白區域(內縮)
| css code | 代表意思 | 整理 |
| --- | --- | --- |
| `margin: 5px` | 其邊界上下左右均留空白5px | `margin: 上下左右` |
| `margin: 5px 10px` | 上下邊界為5px，左右邊界為10px | `margin: 上下 左右` |
| `margin: 5px 4px 10px` | 上邊界為5px，左右邊界各為4px，下邊界為10px | `margin: 上 左右 下` |
| `margin: 5px 4px 6px 10px` | 上邊界為5px，右邊界為4px，下邊界為6px，左邊界為10px | `margin: 上 右 下 左` |

## 對齊方式
- 設定區塊內文字的對齊方式，可用 `text-align` 和 `vertical-align` 屬性
	- `text-align`：設定水平方向的左右對齊
		- `left`：靠左對齊
		- `right`：靠右對齊
		- `center`：置中
		- `justify`：左右兩邊均對齊(瀏覽器會自動調整讓兩邊都能對齊)
	- `vertical-align`：設定垂直方向的上下對齊
		- `top`：向上對齊
		- `bottom`：向下對齊
		- `middle`：向中對齊
		- `super`：設定上標字(例如次方)
		- `sub`：設定下標字

## DIV區塊排列
- 用 `float` 屬性來設定
	- `none`：不做水平排列(預設值)
	- `left`：讓所有區塊由右至左排列
	- `right`：讓所有區塊由左至右排列
- `clear`：指區塊左右不要出現其他 float 的內容
	- `left`：左邊淨空
	- `right`：右邊淨空
	- `both`：兩邊淨空
