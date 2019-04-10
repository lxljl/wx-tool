## 把秒转为 时分秒

#### 1.引入

```
    var {
        formatSeconds
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  value  | string  |        | 是 | 秒 ||

#### 3.使用

```
    formatSeconds(8000000) //  2222小时13分20秒
    formatSeconds(601) //  10分1秒
    formatSeconds(60) //  60秒
    formatSeconds(61) //  1分1秒
```