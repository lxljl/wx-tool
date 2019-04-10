## 通过哈希函数获取用户名的颜色

#### 1.引入

```
    var {
        getUsernameColor
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  username  | string  |        | 是 | 用户名 |
| color  | string |    [
    '#e21400',
    '#91580f',
    '#f8a700',
    '#f78b00',
    '#58dc00',
    '#287b00',
    '#a8f07a',
    '#4ae8c4',
    '#3b88eb',
    '#3824aa',
    '#a700ff',
    '#d300e7',
  ]    | 否 | color数组        |

#### 3.使用

```
    // 使用默认随机颜色
    getUsernameColor('wx')  // #e21400
    getUsernameColor('tb')  // #287b00

    // 自由搭配颜色数组
    getUsernameColor('wx', ['#fff', '#000'])  // #fff
    getUsernameColor('wx', ['#fff', '#000'])  // #000

```