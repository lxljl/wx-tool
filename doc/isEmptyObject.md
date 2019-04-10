## 判断obj是否为空

#### 1.引入

```
    var {
        isEmptyObject
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  obj  | object  |        | 是 | 对象 |

#### 3.使用

```
    isEmptyObject({})  // true

    isEmptyObject({s:2})  // false
```