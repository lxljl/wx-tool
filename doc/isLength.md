## 检测该字符串是否为空

#### 1.引入

```
    var {
        isLength
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
| s | string |        | 是 | 所选的字符串|
| l | number |        | 是 | 所需的长度|

#### 3.使用

```
    isLength('asd', 4)  // false
    isLength('asd', 3)  // true
    isLength('asd', 2)  // true
 
```