## 云函数调用

#### 1.引入

```
    var {
        cloudFn
    } = require('wx-tool')
```

#### 2.参数

|  属性   | 类型    | 默认值 | 必填   | 说明            |
| :-------: | :------: | ------ | :--------: | :--------|
|  name  | string  |        | 是 | 云函数名字 |
| data  | object |        | 否 | 传输的数据         |

#### 3.使用

```

    // 云函数返回格式  创建一个Promise
    resolve({
        code: 0,   // code 为0 是成功， 大于0 则失败
        data: data,  // 返回的数据
        info: '操作成功！'   // 信息提示
    })

    
    // 使用例子
    cloudFn('getList', {
        page: 1,
        limit: 15
    }).then((res)=>{
        console.log(res)
    })

    // 也可以使用 async/await
    async getList(){
        try {
            let result = await cloudFn('getList', {
                page: 1,
                limit: 15
            })
            console.log(result)
        } catch (error) {
            console.log(error)
        }
    }

    调用时 会显示loading提示,  成功或失败之后 消失

```