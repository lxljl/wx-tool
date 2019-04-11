## 云函数微信支付

#### 1.引入

```
    var {
        cloudGetPay
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  fee  | number  |        | 是 | 标价金额  订单总金额，单位为分 |
| attach  | string |        | 是 | 附加数据 例如:深圳分店         |
| body | object |        | 是 | 商品描述  128字节  例如:腾讯充值中心-QQ会员充值|

#### 3.使用


需要搭配云函数 使用   [微信支付云函数](https://github.com/lxljl/cloudFns/blob/master/doc/getPay.md)

```
    // 返回Promise
    await cloudGetPay({
        fee: 0.01,
        attach: '深圳分店',
        body: '腾讯充值中心-QQ会员充值'
    }).then((res)=>{
        console.log(res)
    })


    // 也可以使用 async/await
    async pay(){
        try {
            let result = await cloudGetPay({
                fee: 0.01,
                attach: '深圳分店',
                body: '腾讯充值中心-QQ会员充值'
            })
            支付成功
            console.log(result)
        } catch (error) {
            // 支付失败
            console.log(error)
        }
    }

```