# 设备信息
**模块名称：Device**

## 方法
* [Device.getInfo](#获取设备信息)：获取设备信息

### 获取设备信息
**用法：**`Device.getInfo(successCB, failedCB)`  
**示例：**

```js
    Device.getInfo(function (successObj) {
        console.log(JSON.stringify(successObj, null, 2));
    },function (error) {
        var msg = JSON.stringify(error);
        console.log(msg);
        alert(msg);
    });
```

