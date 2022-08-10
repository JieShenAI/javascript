文本

```javascript
$.ajax({
            url: url,
            type: "POST",
            data: {
                key: "value"
            },
            success: function (data) {
                alert(data);
            }
        });
```

> 若要跨域设置  crossDomain: true

同步操作

async: false;  禁止异步操作，这样可以保证程序的正常流程进行；

除非是获取数据直接就渲染到页面上，这样可以使用异步；

```javascript
$.ajax({
            type: "get",
            url: "/data/areainfo",
            data: {year: year, areaID: areaID},
            async: false,
            success: function (data) {
                areaData = getInfo(data);
            }
});
```

> 需要在django 接受POST传参的python函数前加上`@csrf_exempt`





## 传递嵌套对象

> 上述的POST传参直接传递的对象

`dataType: "json",`
