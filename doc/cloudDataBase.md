## 云数据库调用

#### 1.引入

```
    var {
        cloudDataBase
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  type  | string  |        | 是 | 类型 |
| name  | string |        | 是 | 数据库名字         |
| data | string |        | 否 | 传输的数据|

#### 3.使用

```
    // 返回Promise
    cloudDataBase({
        name: 'user',
        type: 'get',
    }).then((res)=>{
        console.log(res)
        // {
        //     data: {
        //         openid:"ovr-35QuJxxFBl_u7y6UvfZD9eXU"
        //         session_key:"mDF1mfMXu9mdyh1DpXqHEg=="
        //         unionid:"ozyLx0_onADv0lhK2CUeiCe34UH4"
        //         _id:"ovr-35QuJxxFBl_u7y6UvfZD9eXU"
        //     },
        //     errMsg:"collection.get:ok"  
        // }
    })

    // 也可以使用 async/await
    async test(){
        try {
            // 获取用户列表
            let data = await cloudDataBase({
                name: 'user',
                type: 'get',
            })
            console.log(data)
        } catch (error) {
            console.log(error)
        }
    }

```
### 更多例子

* 新增记录 
```
    try{
        // 新增用户
        let data = await cloudDataBase({
            name: 'user',
            type: 'add',
            data: {
                session_key:"mDF1mfMXu9mdyh1DpXqHEg==",
                unionid:"ozyLx0_onADv0lhK2CUeiCe34UH4"
            }
        })
    } catch (error) {
        console.log(error)
    }
```

* 查找记录 
```
    try{
        // 根据条件查找用户
        let data = await cloudDataBase({
            name: 'user',
            type: 'where',
            data: {
                "openid": "ovr-35QuJxxFBl_u7y6UvfZD9eXU"
            }
        }).get()
        或者 根据id查找用户
        let data = await cloudDataBase({
            name: 'user',
            type: 'doc',
            data: 'f4cf49925cad673f0364c3a023dbf06b'
        }).get()
    } catch (error) {
        console.log(error)
    }
```

* 删除记录 
```
    // 小程序端只可删除单条记录，如果需删除多条记录，需使用云函数端 API
    try{
        let data = await cloudDataBase({
            name: 'user',
            type: 'doc',
            data: 'f4cf49925cad673f0364c3a023dbf06b'
        }).remove()
    } catch (error) {
        console.log(error)
    }
```

* 更新一条记录 
```
    // 小程序端只可更新单条记录，如果需更新多条记录，需使用云函数端 API
    try{
        let data = await cloudDataBase({
            name: 'user',
            type: 'doc',
            data: 'f4cf49925cad67660364de0231365506'
        }).update({
            data: {
                session_key: "1212121113",
            }
        })
    } catch (error) {
        console.log(error)
    }
```

* 替换更新一条记录
```
    try{
        let data = await cloudDataBase({
            name: 'user',
            type: 'doc',
            data: 'f4cf49925cad67660364de0231365506'
        }).set({
            data: {
                session_key: "1212121113",
                asdsadsad: "123123"
            }
        })
    } catch (error) {
        console.log(error)
    }
```