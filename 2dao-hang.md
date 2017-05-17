# 导航
**模块名称：Navigation**

## 方法
* [Navigation.logout](#退出登录)：退出登录
* [Navigation.changePassword](#修改密码)：修改密码
* [Navigation.getCookie](#获取cookie)：获取cookie
* [Navigation.setOrientation](#设置屏幕方向)：设置屏幕方向

### 退出登录
**用法：**`Navigation.logout(successCB, failedCB)`
**示例：**

```js
    Navigation.logout(function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

### 修改密码
**用法：**`Navigation.changePassword(successCB, failedCB)`
**示例：**

```js
    Navigation.changePassword(function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

### 获取cookie
**支持平台**：iOS
**用法：**`Navigation.getCookie(successCB, failedCB)`
**示例：**

```js
    Navigation.getCookie(function (obj) {
        console.log(JSON.stringify(Obj));
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

### 设置屏幕方向
**用法：**`Navigation.setOrientation(orientation,successCB, failedCB)`
**参数：**
`orientation` 可选项：

    值 | 描述
    --- | ---
    0 | 竖屏 Portrait
    1 | 倒屏 Upside Down（iOS有效）
    2 | 左横屏 Landscape Left
    3 | 右横屏 Landscape Right

**示例：**

```js
    //orientation: 0-Portrait,1-Upside Down,2-Landscape Left,3-Landscape Right
    Navigation.setOrientation(2, function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```