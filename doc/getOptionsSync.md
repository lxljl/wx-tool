## 获取小程序启动时的参数

#### 1.引入

```
    var {
        getOptionsSync
    } = require('wx-tool')
```

#### 2.使用

```
    // 等同于 wx.getLaunchOptionsSync
    getOptionsSync()

    返回
    {
        "path": "xxx", 启动小程序的路径
        "scene": "xxx", 启动小程序的场景值
        "query": "xxx", 启动小程序的 query 参数
        "shareTicket": "xxx", shareTicket，转发信息
        "referrerInfo": {
            appId: "xxx",
            extraData: "xxx"
        }, 来源信息。从另一个小程序、公众号或 App 进入小程序时返回。否则返回 {}
    }

```