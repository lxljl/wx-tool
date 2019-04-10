## 对象序列化

#### 1.引入

```
    var {
        stringfyQueryString
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  obj  | object  |        | 是 | 对象 |

#### 3.使用

```
    stringfyQueryString({
        a: 2,
        b: 3
    })

    // a=2&b=3

```