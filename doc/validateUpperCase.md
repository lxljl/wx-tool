## 是否大小写字母

#### 1.引入

```
    var {
        validateUpperCase
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  s  | string  |        | 是 | 提示的内容 |

#### 3.使用

```
    validateUpperCase('a') // false
    validateUpperCase('b') // false
    validateUpperCase('c') // false
    validateUpperCase('A') // true
    validateUpperCase('B') // true

```