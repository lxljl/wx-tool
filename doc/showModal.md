## 显示模态对话框

#### 1.引入

```
    var {
        showModal
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  title  | string  |        | 是 | 提示的标题 |
| content  | string |        | 否 | 提示的内容         |
| showCancel | string |    true    | 否 | 是否显示取消按钮|
| cancelText | string |   取消     | 否 |  取消按钮的文字，默认为"取消"，最多 4 个字符|
| cancelColor | string |   #000000     | 否 |  取消按钮的文字颜色，默认为"#000000" |
| confirmText | string |   确定     | 否 |  确定按钮的文字，默认为"确定"，最多 4 个字符 |
| confirmColor | string |   #00aaff     | 否 |  确定按钮的文字颜色，默认为"#00aaff" |

#### 3.使用

```
    // 等同于 wx.showModal
    // 返回Promise
    showModal({
        title: `提示`,
        content: '支付成功',
        showCancel: false
    }).then((res)=>{
        console.log(res)
    })


    // 也可以使用 async/await
    async test(){
        try {
            let {
                confirm
            } = await showModal({
                title: '提示',
                content: `是否确认收货？`
            })
            if(confirm) {
                // 用户点击确认


                //你的代码....
            }
        } catch (error) {
            console.log(error)
        }
    }

```