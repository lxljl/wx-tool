## 是否大小写字母

#### 1.引入

```
    var {
        validatAlphabets
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  s  | string  |        | 是 | 传入字符串 |

#### 3.使用

```
    validatAlphabets('a')   // true
    validatAlphabets('A')   // true
    validatAlphabets('Aa')   // true
    validatAlphabets('Aas2') // false

```