# 导航
**模块名称：Navigation**

****

## 方法
* Navigation.logout
* Navigation.changePassword
* Navigation.getCookie
* Navigation.setOrientation

****

## 退出登录
`Navigation.logout(successCB, failedCB)`

example:

```js
    Navigation.logout(function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

****

## 密码修改
`Navigation.changePassword(successCB, failedCB)`

example:

```js
    Navigation.changePassword(function () {
        console.log("成功");
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

****

## 获取cookie（iOS）
`Navigation.getCookie(successCB, failedCB)`

example:

```js
    Navigation.getCookie(function (obj) {
        console.log(JSON.stringify(Obj));
    }, function (errorObj) {
        console.log(JSON.stringify(errorObj));
    });
```

****

## 设置屏幕方向
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

****