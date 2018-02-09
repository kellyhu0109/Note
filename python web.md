python web
==
- url = localhost:9999/hello
- \<name\> 為自己輸入的值會帶進 return 中

```python=
from bottle import route, run  
  
@route('/hello/<name>') #定義路由，即瀏覽器訪問的地址，localhost:9999/hello  
def home(name):  
    return 'hello %s, this is my home page' % name  
  
run(host='localhost', port=9999)

```

```python=
from bottle import route, run, static_file #導入html檔案

@route('/')
def home():
    return static_file('index.html',root='.')

run(host='localhost', port=9999)
```

