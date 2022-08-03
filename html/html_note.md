# 標籤
| 標籤 | 意義 |
| --- | --- |
| \<p\> ... \</p\> | 段落 |
| \<br\> | 換行 |
| \<a href="google.com"\> ... \</a\> | 超連結 |
| \<img src="img_url"\> | 段落 |
| \<!-- ... --\> | 註解 |
| \<pre\> ... \</pre\> | 依照原有的空白、換行顯示 |
| \<input type="" name="" value=""\> | 輸入方塊、送出按鈕 |

## 表單
> 表示方式：\<from\> ... \</from\>
- 在寫form時，必要的兩個屬性
    - action
        - 設定表單資料要送到哪裡
    - method
        - 設定資料送出的方式
            - get
                - 若是使用 HTTP 通訊協定中的 GET 方法送出資料，**使用者傳送的資料會以附在 URL 內的方式(明碼)傳送，會有資安的疑慮、不安全**，且不能傳送超過 1024 bytes 的資料。
            - post ==recommend==
                - 使用 HTTP 通訊協定中的 POST 方法傳送資料，會將**使用者輸入的資料附加於 HTTP 的通訊檔頭送出，較安全**，且沒有傳送的大小限制。
```html=
<form action='' method=''>
    ...
</form>
```
## 輸入框 input
> 表示方式：\<input type="" name="" value=""\>
- 屬性
    - type：種類，可以分為一般輸入、密碼模式、按鈕
    - name：欄位名稱
        - 一般輸入框傳送文字：`<input type="text" name="username">`
        - 密碼：`<input type="password" name="password">`
        - 按鈕：
            - 送出：`<input type="submit" name="">`
            - 重設：`<input type="reset" name="">`
            - 單選紐(radio)：`<input type="radio" name="">[要顯示的選項名稱]`
            - 多選紐(checkbox)：`<input type="checkbox" name="">[要顯示的選項名稱]`
            - [how to solve multi checkbox in server?](https://stackoverflow.com/questions/18745456/handle-multiple-checkboxes-with-a-single-serverside-variable)
    - value：預設文字 
- 多行輸入
    - 可設定欄數(cols)、行數(rows)
    - `<textarea name="note" cols="30px" rows="5"></textarea>`

# 特殊字元表示法
| 要顯示的字元或符號 | HTML文件中的特殊寫法 |
| --- | --- |
| < | \&lt; |
| > | \&gt; |
| " | \&quot; |
| 空白 | \&nbsp; |