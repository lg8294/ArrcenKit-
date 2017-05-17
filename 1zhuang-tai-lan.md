# 状态栏
**模块名称：StatusBar**
[ngcordova](https://www.npmjs.com/package/cordova-plugin-statusbar)
[使用说明](https://github.com/apache/cordova-plugin-statusbar)

## 属性

* StatusBar.isVisible

## 方法

* StatusBar.overlaysWebView
* StatusBar.styleDefault
* StatusBar.styleLightContent
* StatusBar.styleBlackTranslucent
* StatusBar.styleBlackOpaque
* StatusBar.backgroundColorByName
* StatusBar.backgroundColorByHexString
* StatusBar.hide
* StatusBar.show

### 状态栏文本颜色
example:

```js
    StatusBar.styleDefault(); // 黑色文本
    StatusBar.styleLightContent(); // 白色文本
```

### 状态栏颜色
example:

```js
    StatusBar.backgroundColorByHexString("#333"); // => #333333
    StatusBar.backgroundColorByHexString("#FAB"); // => #FFAABB
```

### 状态栏隐藏和显示

example - 隐藏:

```js
    StatusBar.hide();//隐藏
```

example - 显示:

```js
    StatusBar.show();//显示
```