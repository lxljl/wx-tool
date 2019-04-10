## 读取本地文件内容

#### 1.引入

```
    var {
        localEncoding
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  filePath  | string  |        | 是 | 要读取的文件的路径 |
| encoding  | string |    base64    | 否 | 指定读取文件的字符编码，如果不传 encoding，则以 ArrayBuffer 格式读取文件的二进制内容 ascii / base64 / binary / hex / (ucs2/ucs-2/utf16le/utf-16le) / utf-8/utf8 / latin1         |

#### 3.使用

```
    localEncoding('微信小程序临时路径')
    localEncoding('微信小程序临时路径', 'ascii')

```