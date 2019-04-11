# wx-tool

微信小程序工具类集合，有效提高开发时间和效率!


## 另推荐[云函数合集](https://github.com/lxljl/cloudFns)模板


**重要：版本要求**

1. 小程序基础库版本 2.2.3 或以上
2. 开发者工具 1.02.1808300 或以上开始，小程序支持使用 npm 安装第三方包。


使用微信开发者工具打开此项目，然后在项目根目录下运行：
```bash
npm install --production
```

安装好依赖包之后，点击工具顶部菜单栏的详情：

![image](https://github.com/lxljl/wx-tool/blob/master/doc/image/1.png)

勾选“使用 npm 模块”选项：

![image](https://github.com/lxljl/wx-tool/blob/master/doc/image/2.png)

最后点击开发者工具中的菜单栏：工具 --> 构建 npm 即可运行。

![image](https://github.com/lxljl/wx-tool/blob/master/doc/image/3.png)


#### 1.快速开始
```
    $ npm i wx-tool --save
```

#### 2.按需引入

```
    var {
        showModal
    } = require('wx-tool')
```

#### 3.使用例子

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  title  | string  |        | 是 | 提示的标题 |
| content  | string |        | 否 | 提示的内容         |
| showCancel | string |    true    | 否 | 是否显示取消按钮|
| cancelText | string |   取消     | 否 |  取消按钮的文字，默认为"取消"，最多 4 个字符|
| cancelColor | string |   #000000     | 否 |  取消按钮的文字颜色，默认为"#000000" |
| confirmText | string |   确定     | 否 |  确定按钮的文字，默认为"确定"，最多 4 个字符 |
| confirmColor | string |   #00aaff     | 否 |  确定按钮的文字颜色，默认为"#00aaff" |


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


## API

* showToast --- [显示消息提示框](https://github.com/lxljl/wx-tool/blob/master/doc/showToast.md)
* showModal --- [显示模态对话框](https://github.com/lxljl/wx-tool/blob/master/doc/showModal.md)
* requestPayment --- [微信支付](https://github.com/lxljl/wx-tool/blob/master/doc/requestPayment.md)
* cloudGetPay --- [云函数微信支付](https://github.com/lxljl/wx-tool/blob/master/doc/cloudGetPay.md)
* localEncoding --- [读取本地文件内容](https://github.com/lxljl/wx-tool/blob/master/doc/localEncoding.md)
* arrayEqual --- [判断两个数组是否相等](https://github.com/lxljl/wx-tool/blob/master/doc/arrayEqual.md)
* isEmptyObject --- [判断obj是否为空](https://github.com/lxljl/wx-tool/blob/master/doc/isEmptyObject.md)
* randomColor --- [随机生成颜色](https://github.com/lxljl/wx-tool/blob/master/doc/randomColor.md)
* randomNum --- [生成指定范围随机数](https://github.com/lxljl/wx-tool/blob/master/doc/randomNum.md)
* bankSpace --- [银行卡每四位+空格](https://github.com/lxljl/wx-tool/blob/master/doc/bankSpace.md)
* getOptionsSync --- [获取小程序启动时的参数](https://github.com/lxljl/wx-tool/blob/master/doc/getOptionsSync.md)
* trim --- [去除两端空格](https://github.com/lxljl/wx-tool/blob/master/doc/trim.md)
* isNew --- [检测是否是新版本](https://github.com/lxljl/wx-tool/blob/master/doc/isNew.md)
* isNum --- [检测数字](https://github.com/lxljl/wx-tool/blob/master/doc/isNum.md)
* isPhone --- [检测该手机号是否正确](https://github.com/lxljl/wx-tool/blob/master/doc/isPhone.md)
* isMail --- [检测该邮箱是否正确](https://github.com/lxljl/wx-tool/blob/master/doc/isMail.md)
* isPlate --- [检测该车牌号是否正确](https://github.com/lxljl/wx-tool/blob/master/doc/isPlate.md)
* isIdCard --- [判断是否为身份证](https://github.com/lxljl/wx-tool/blob/master/doc/isIdCard.md)
* validateURL --- [合法uri](https://github.com/lxljl/wx-tool/blob/master/doc/validateURL.md)
* validateLowerCase --- [是否小写字母](https://github.com/lxljl/wx-tool/blob/master/doc/validateLowerCase.md)
* validateUpperCase --- [是否大写字母](https://github.com/lxljl/wx-tool/blob/master/doc/validateUpperCase.md)
* validatAlphabets --- [是否大小写字母](https://github.com/lxljl/wx-tool/blob/master/doc/validatAlphabets.md)
* digitUppercase --- [现金额转大写](https://github.com/lxljl/wx-tool/blob/master/doc/digitUppercase.md)
* decimalAdd --- [浮点数相加](https://github.com/lxljl/wx-tool/blob/master/doc/decimalAdd.md)
* getDistance --- [计算两点的距离](https://github.com/lxljl/wx-tool/blob/master/doc/getDistance.md)
* uuid --- [返回一个v4兼容的UUID](https://github.com/lxljl/wx-tool/blob/master/doc/uuid.md)
* getUsernameColor --- [通过哈希函数获取用户名的颜色](https://github.com/lxljl/wx-tool/blob/master/doc/getUsernameColor.md)
* isLength --- [检测该字符串是否为空](https://github.com/lxljl/wx-tool/blob/master/doc/isLength.md)
* formatSeconds --- [把秒转为 时分秒](https://github.com/lxljl/wx-tool/blob/master/doc/formatSeconds.md)
* parseTime --- [格式化时间](https://github.com/lxljl/wx-tool/blob/master/doc/parseTime.md)
* formatTime --- [返回目标时间距离当前时间时长](https://github.com/lxljl/wx-tool/blob/master/doc/formatTime.md)
* stringfyQueryString --- [对象序列化](https://github.com/lxljl/wx-tool/blob/master/doc/stringfyQueryString.md)
* isBack --- [该页面是否可以返回上一页](https://github.com/lxljl/wx-tool/blob/master/doc/isBack.md)
* successBack --- [成功后返回上一页](https://github.com/lxljl/wx-tool/blob/master/doc/successBack.md)
* getQueryString --- [获取url参数](https://github.com/lxljl/wx-tool/blob/master/doc/getQueryString.md)
* bMapTransQQMap --- [百度地图经纬度转腾讯地图经纬度](https://github.com/lxljl/wx-tool/blob/master/doc/bMapTransQQMap.md)
* qqMapTransBMap --- [腾讯地图经纬度转百度地图经纬度](https://github.com/lxljl/wx-tool/blob/master/doc/qqMapTransBMap.md)
* cloudFn --- [云函数调用](https://github.com/lxljl/wx-tool/blob/master/doc/cloudFn.md)
* cloudDataBase --- [云数据库调用](https://github.com/lxljl/wx-tool/blob/master/doc/cloudDataBase.md)
* makePy --- [提取中文首字母](https://github.com/lxljl/wx-tool/blob/master/doc/makePy.md)