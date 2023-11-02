# 开发文档

当前版本：v5（最新）
说明：T1 后端云完全免费，无任何限制，使用需绑定自己已备案的域名，可以联系客服绑定（免费），软件开发期间可以使用以下域名代替：

```bash
http://dev.t1y.net/api
```

获取服务器时间：

```bash
http://dev.t1y.net/api/timestamp
```

Go 语言 SDK：https://github.com/t1ykf/t1y-sdk-go

Vite4+Vue3+TypeScript 封装例子（已全部封装）：https://github.com/t1ykf/t1-vite-vue-typescript-demo

更多 SDK 及 功能 持续加入中，期待您的加入……

### 注册 T1 后端云账号

在网址栏输入 dev.t1y.net 或者在百度输入 T1 后端云搜索，打开 T1 后端云 官网后，登录或注册账号，即可进入仪表盘。
![alt 登录或注册](./images/1.png)

### 创建应用

登录账号进入 T1 仪表盘后，点击仪表盘界面左上角“创建应用”，在弹出框输入您应用的名称和类型后确认，您就拥有了一个专业版的应用。
![alt 创建应用](./images/2.png)

### 获取应用密钥

点击您要查看密钥的应用右边的查看密钥按钮，即可查看密钥。
![alt 查看密钥](./images/3.png)
获取 Application ID 和 API Key 以及 Secret Key，Application ID 以及 API Key 将在后面用于 RESTful API 请求中作为 HTTP 头部的 X-T1Y-Application-ID 和 X-T1Y-Api-Key 的值传到接口。

### 预览管理应用数据

点击开发按钮，即可进入预览与数据管理页面，你可以很轻松的管理各类数据。
![alt 预览与管理数据](./images/4.png)

### 添加一行数据

```shell
curl -X POST \
    -H "X-T1Y-Application-ID: Your Application ID" \
    -H "X-T1Y-Api-Key: Your Api Key" \
    -H "X-T1Y-Safe-NonceStr: Client random code" \
    -H "X-T1Y-Safe-Timestamp: Current timestamp" \
    -H "X-T1Y-Safe-Sign: MD5(Path + Application ID + API Key + NonceStr + Timestamp + Secret_Key)" \
    -H "Content-Type: application/json" \
    -d '{"score":1337,"playerName":"Sean Plott","cheatMode":false}' \
    https://自己备案的域名/v5/classes/YourTableName
```

### 删除一行数据

```shell
curl -X DELETE \
    -H "X-T1Y-Application-ID: Your Application ID" \
    -H "X-T1Y-Api-Key: Your Api Key" \
    -H "X-T1Y-Safe-NonceStr: Client random code" \
    -H "X-T1Y-Safe-Timestamp: Current timestamp" \
    -H "X-T1Y-Safe-Sign: MD5(Path + Application ID + API Key + NonceStr + Timestamp + Secret_Key)" \
    -H "Content-Type: application/json" \
    https://自己备案的域名/v5/classes/YourTableName/ObjectID
```

### 修改一行数据

```shell
curl -X PUT \
    -H "X-T1Y-Application-ID: Your Application ID" \
    -H "X-T1Y-Api-Key: Your Api Key" \
    -H "X-T1Y-Safe-NonceStr: Client random code" \
    -H "X-T1Y-Safe-Timestamp: Current timestamp" \
    -H "X-T1Y-Safe-Sign: MD5(Path + Application ID + API Key + NonceStr + Timestamp + Secret_Key)" \
    -H "Content-Type: application/json" \
    -d '{"$set":{"score":1337,"playerName":"Sean Plott","cheatMode":false}}' \
    https://自己备案的域名/v5/classes/YourTableName/ObjectID
```

### 获取一行数据

```shell
curl -X GET \
    -H "X-T1Y-Application-ID: Your Application ID" \
    -H "X-T1Y-Api-Key: Your Api Key" \
    -H "X-T1Y-Safe-NonceStr: Client random code" \
    -H "X-T1Y-Safe-Timestamp: Current timestamp" \
    -H "X-T1Y-Safe-Sign: MD5(Path + Application ID + API Key + NonceStr + Timestamp + Secret_Key)" \
    -H "Content-Type: application/json" \
    https://自己备案的域名/v5/classes/YourTableName/ObjectID
```

### 获取全部数据（分页查询）

```shell
curl -X GET \
    -H "X-T1Y-Application-ID: Your Application ID" \
    -H "X-T1Y-Api-Key: Your Api Key" \
    -H "X-T1Y-Safe-NonceStr: Client random code" \
    -H "X-T1Y-Safe-Timestamp: Current timestamp" \
    -H "X-T1Y-Safe-Sign: MD5(Path + Application ID + API Key + NonceStr + Timestamp + Secret_Key)" \
    -H "Content-Type: application/json" \
    https://自己备案的域名/v5/classes/YourTableName?page=1&size=10
```

### X-T1Y-Safe-Sign 加密格式说明

X-T1Y-Safe-Sign 用于生成签名，确保数据安全。你应当使用 URL 中的路径（注意 GET 参数不需要参与运算）+您的 Application ID+您的 API Key+NonceStr（这是客户端随机生成的 32 位字符串）+Timestamp（当前时间戳，精确到秒即可）+您的 SecretKey 进行 MD5 取值，就得到了 X-T1Y-Safe-Sign 的值。

**举例：查询全部数据**
查询 student 表中的第 1 页的 10 条数据

```bash
http://自己备案的域名/v5/classes/student?page=1&size=10
```

这时 X-T1Y-Safe-Sign 的值就应当为以下内容的 MD5 运算结果：

```js
MD5(
  "/v5/classes/student" +
    Application_ID +
    API_Key +
    NonceStr +
    Timestamp +
    Secret_Key
);
```

### 快速参考表

![alt 快速参考表](./images/5.png)

### 联系我们

联系
网站：dev.t1y.net
邮箱：wwwanghua@outlook.com
QQ：422584084
微信：wwwAnghuaWechat
QQ 交流群 1：671186603
QQ 交流群 2：292846194
Github 组织：https://github.com/t1ykf
