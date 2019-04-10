## 获取url参数

#### 1.引入

```
    var {
        getQueryString
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  location  | string  |        | 是 | url |
| key  | string |        | 否 | 所需要的key         |

#### 3.使用

```
    getQueryString('https://mp.weixin.qq.com?a=1&b=2&c=3')  //  {a: "1", b: "2", c: "3"}
    
    getQueryString('https://mp.weixin.qq.com?a=1&b=2&c=3', 'a') // 1 

```