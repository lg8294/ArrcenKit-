# 导航
**模块名称：Navigation**

## 方法
* [Navigation.logout](#退出登录)：退出登录
* [Navigation.changePassword](#修改密码)：修改密码
* [Navigation.getCookie](#获取cookie)：获取cookie
* [Navigation.setOrientation](#设置屏幕方向)：设置屏幕方向

### 退出登录
`Navigation.logout(successCB, failedCB)`

example:

```js
    Navigation.logout(function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

### 修改密码
`Navigation.changePassword(successCB, failedCB)`

example:

```js
    Navigation.changePassword(function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

### 获取cookie
**支持平台**：iOS

`Navigation.getCookie(successCB, failedCB)`

example:

```js
    Navigation.getCookie(function (obj) {
        console.log(JSON.stringify(Obj));
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

### 设置屏幕方向
`Navigation.setOrientation(orientation,successCB, failedCB)`

`orientation` 可选项：

    参数 | 描述
    --- | ---
    0 | 竖屏 Portrait
    1 | 倒屏 Upside Down（iOS有效）
    2 | 左横屏 Landscape Left
    3 | 右横屏 Landscape Right

example:

```js
    //orientation: 0-Portrait,1-Upside Down,2-Landscape Left,3-Landscape Right
    Navigation.setOrientation(2, function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```