# 图片选择器
**模块名称：imagePicker**
[ngcordova](http://ngcordova.com/docs/plugins/imagePicker)
[使用说明](https://github.com/wymsee/cordova-imagePicker)

****

### 方法
* window.imagePicker.getPictures

****

### 选择图片
`window.imagePicker.getPictures(successCB, failureCB[, options])`

`options` 可选项：

    key | 描述
    ---- | ----
    maximumImagesCount | 最大选择数量，默认15
    width | 图片宽度，默认800px
    height | 图片高度，默认800px
    quality | 图片质量（0-100），默认100


example - Get Full Size Images (all default options):

```js
    window.imagePicker.getPictures(function(results) {
      console.log(JSON.stringify(results, null, 2));
    }, function (error) {
      var msg = JSON.stringify(error);
      console.log(msg);
      alert(msg);
    });
```

example - Get at most 10 images scaled to width of 800:

```js
    window.imagePicker.getPictures(function(results) {
      for (var i = 0; i < results.length; i++) {
        console.log('Image URI: ' + results[i]);
      }
    }, function (error) {
      console.log('Error: ' + error);
    }, {
      maximumImagesCount: 10,
      width: 800
    });
```

****


