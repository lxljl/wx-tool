## 合法uri

#### 1.引入

```
    var {
        validateURL
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  s  | string  |        | 是 | 传入url |

#### 3.使用

```
    validateURL('https://mp.weixin.qq.com') // true
    validateURL('https://mp.weixin.qq.c') // false
    validateURL('https://mp.weixin.qq..com') // false
    validateURL('htt://mp.weixin.qq.com') // false

```