## 显示消息提示框

#### 1.引入

```
    var {
        showToast
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  title  | string  |        | 是 | 提示的内容 |
| icon  | string |    success    | 否 | 图标 默认 success ，可选none         |
| image | string |        | 否 | 自定义图标的本地路径，image 的优先级高于 icon|
| duration | number |   1500     | 否 | 提示的延迟时间|
| mask | boolean |   true     | 否 |  是否显示透明蒙层，防止触摸穿透 |

#### 3.使用

```
    // 等同于 wx.showToast
    // 返回Promise
    showToast({
        title: `成功`,
        icon: 'success'
    }).then((res)=>{
        console.log(res)
    })


    // 也可以使用 async/await
    async test(){
        try {
            await showToast({
                title: '支付成功',
                content: `是否确认收货？`
            })
            // 返回上一页
            wx.navigateBack()
        } catch (error) {
            console.log(error)
        }
    }

```