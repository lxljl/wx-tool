## 显示消息提示框

#### 1.引入

```
    var {
        isMail
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  s  | string  |        | 是 | 所选邮箱 |

#### 3.使用

```
    isMail('lxx_ljl@163.com') // true
    isMail('l@163..asd..comasd') // false

```