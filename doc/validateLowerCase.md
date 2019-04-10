## 是否小写字母

#### 1.引入

```
    var {
        validateLowerCase
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  s  | string  |        | 是 | 提示的内容 |

#### 3.使用

```
    validateLowerCase('a') // true
    validateLowerCase('b') // true
    validateLowerCase('c') // true
    validateLowerCase('A') // false
    validateLowerCase('B') // false

```