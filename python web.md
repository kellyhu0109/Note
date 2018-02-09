```python=
from bottle import route, run  
  
@route('/hello/<name>') #定義路由，即瀏覽器訪問的地址，localhost:9999/hello  
def home(name):  
    return 'hello %s, this is my home page' % name  
  
run(host='localhost', port=9999)

```
