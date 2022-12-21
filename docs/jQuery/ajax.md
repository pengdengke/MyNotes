## ajax 同步/异步请求

```JavaScript
var result = {}
$.ajax({
    async: false,  // true-异步, false-同步
    type: 'POST',
    url: url,
    data: data,
    dataType: 'json',
    success: function (json) {
        result = json
    },
    error: function () {
        result = {"code": -1, "msg": "请求失败"}
    }
});
```

## 序列化表单

1. serialize() 方法
```JavaScript
// 将表单内容序列化成一个字符串, 例如 param1=value1&param2=value2
var data = $("#form_id").serialize()
```
2. serializeArray() 方法
```JavaScript
// 将页面表单序列化成一个JSON结构的对象。注意不是JSON字符串, 例如[{"name":"lihui"},{...}]
var jsonData  = $("#form_id").serializeArray()  
```