## 微信支付

#### 1.引入

```
    var {
        requestPayment
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  timeStamp  | string  |        | 是 | 时间戳，从 1970 年 1 月 1 日 00:00:00 至今的秒数，即当前的时间 |
| nonceStr  | string |        | 是 | 随机字符串，长度为32个字符以下         |
| package | string |        | 是 | 统一下单接口返回的 prepay_id 参数值，提交格式如：prepay_id=***|
| signType | string |   MD5     | 否 | 签名算法|
| paySign | boolean |        | 是 |  签名，具体签名方案参见 [小程序支付接口文档](https://pay.weixin.qq.com/wiki/doc/api/wxa/wxa_api.php?chapter=7_7&index=3) |

#### 3.使用

```
    // 等同于 wx.requestPayment
    // 返回Promise
    requestPayment({
        timeStamp: 'xxx',
        nonceStr: 'xxx',
        package: 'xxx',
        signType: 'MD5',
        paySign: 'xxx'
    }).then((res)=>{
        console.log(res)
    })


    // 也可以使用 async/await
    async test(){
        try {
            let result = await requestPayment({
                timeStamp: 'xxx',
                nonceStr: 'xxx',
                package: 'xxx',
                signType: 'MD5',
                paySign: 'xxx'
            })
            // 支付成功 返回结果
            console.log(result)
        } catch (error) {
            console.log(error)
        }
    }

```