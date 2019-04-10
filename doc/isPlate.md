## 检测该车牌号是否正确

#### 1.引入

```
    var {
        isPlate
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  s  | string  |        | 是 | 提示的内容 |

#### 3.使用

```
    isPlate('粤A12345')  // true
    isPlate('粤A00000')  // true
    isPlate('粤A345')  // false
    isPlate('BADA345')  // false

```