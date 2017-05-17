# 消息
**模块名称：IMClient**

## 方法
* [IMClient.regist](#验证用户)：验证用户
* [IMClient.receiveMessage](#接收消息回调)：接收消息回调
* [IMClient.sendChatMessage](#发送单聊消息)：发送单聊消息
* [IMClient.sendRoomMessage](#发送群聊消息)：发送群聊消息
* [IMClient.sendRoomMessage](#发送通知消息)：发送通知消息
* [IMClient.sendFriendApply](#发送好友请求)：发送好友请求

### 验证用户
**说明：**前端不要调用，框架已经包含了用户验证功能。  
**用法：**`IMClient.regist(targetId, project, successCB, failedCB)`  
**参数：**

option | 类型 | 描述
--- | ---| ---
targetId | `String` | 用户ID，跟用户注册到IM的ID保持一致
project | `String` | 项目唯一标识名称（包名）
successCB | `Function` | 成功回调
failedCB | `Function` | 失败回调

**示例：**

```js
    IMClient.regist("15196614938", "net.arrcencloud.demo", function (result) {
        console.log(JSON.stringify(result));
    }, function (error) {
        alert(JSON.stringify(error));
    });
```

### 接收消息回调
**用法：**`IMClient.receiveMessage(receiveCB, errorCB)`  
**参数：**

option | 描述
--- | ---
receiveCB | `function` 接收回调
failedCB | `function` 失败回调

**示例：**

```js
    IMClient.receiveMessage(function(msgObj){
        console.log(JSON.stringify(msgObj));
    }, function(error){
        alert(JSON.stringify(error));
    });
```

### 发送单聊消息
**用法：**`IMClient.sendChatMessage(msg, msgType, targetId, project, voiceLength, successCB, failedCB)`  
**参数：**

option | 描述
--- | ---
msg | `string` 消息内容
msgType | `string` 信息类型，可自行匹配多方参数值
targetId | `string` 接收者ID（跟注册IM时的ID保持一致）
project | `string` 项目唯一标识名称（跟注册时保持一致）
voiceLength | `int` 语音消息时间长度，在发送语音消息时有效，单位秒
successCB | `function` 成功回调
failedCB | `function` 失败回调

**示例：**

```js
    IMClient.sendChatMessage("hello world",'text',"15196614938","net.arrcencloud.demo",0,function (successObj) {
        console.log(JSON.stringify(successObj));
    }, function (error) {
        alert(JSON.stringify(error));;
    });
```

### 发送群聊消息
**用法：**`IMClient.sendRoomMessage(msg, msgType, targetId, pass, voiceLength, successCB, failedCB)`  
**参数：**

option | 描述
--- | ---
msg | `string` 消息内容
msgType | `string` 信息类型，可自行匹配多方参数值
targetId | `string` 接收者ID（房间ID，必须事先注册完成好，系统将会返回）
pass | `string` 群聊房间密码
voiceLength | `int` 语音消息时间长度，在发送语音消息时有效，单位秒
successCB | `function` 成功回调
failedCB | `function` 失败回调

**示例：**

```js
    IMClient.sendRoomMessage("hello world",'text',"12345678","12345678",0,function (successObj) {
        console.log(JSON.stringify(successObj));
    }, function (error) {
        alert(JSON.stringify(error));;
    });
```

### 发送通知消息
**用法：**`IMClient.sendInformsMessage(msg, msgType, targetIds, project, title, pushType, successCB, failedCB)`  
**参数：**

option | 描述
--- | ---
msg | `string` 信息类容
msgType | `strinig` 信息类型
targetIds | `array` 接收者Id集合
project | `string` 使用该系统的应用唯一标识
title | `string` 通知标题
pushType | `string` 通知类型 值由业务定义 比如新闻的值为news
successCB | `function` 成功回调
failedCB | `function` 失败回调

**示例：**

```js
    IMClient.sendInformsMessage("hello world",'text',["15196614938","18381674033"],"net.arrcencloud.demo",'通知标题', 'NEWS', function (successObj) {
        console.log(JSON.stringify(successObj));
    }, function (error) {
        alert(JSON.stringify(error));;
    });
```

### 发送好友请求
**用法：**`IMClient.sendFriendApply(msg, ftype, targetId, project, successCB, failedCB)`  
**参数：**

option | 描述
--- | ---
msg | `string` 消息内容
fType | `string` 好友关系类型，自定义，如：text
targetId | `string` 接收者Id
project | `string` 项目名称
voiceLength | `int` 语音消息时间长度，在发送语音消息时有效，单位秒
successCB | `function` 成功回调
failedCB | `function` 失败回调

**示例：**

```js
    IMClient.sendFriendApply("hello world","friend","15196614938","net.arrcencloud.demo",function (successObj) {
       console.log(JSON.stringify(successObj));
    }, function (error) {
       alert(JSON.stringify(error));;
    });
```

