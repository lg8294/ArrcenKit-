## 6.多媒体
**模块名称：==capture==**
[ngcordova](http://ngcordova.com/docs/plugins/capture/)
[使用说明](https://github.com/apache/cordova-plugin-media-capture)

****

#### 方法
* navigator.device.capture.captureAudio
* navigator.device.capture.captureImage
* navigator.device.capture.captureVideo

****

#### 拍照
`navigator.device.capture.captureImage(successCB, failedCB[, options])`

`options` 可选项：

    key | 描述
    ---- | ----
    limit | 拍摄图片的最大数量，默认1（支持Android）
    
example:

```js
    // capture callback
    var captureSuccess = function(mediaFiles) {
        var i, path, len;
        for (i = 0, len = mediaFiles.length; i < len; i += 1) {
            path = mediaFiles[i].fullPath;
            // do something interesting with the file
            console.log(path);
        }
    };

    // capture error callback
    var captureError = function(error) {
        alert('Error code: ' + error.code, null, 'Capture Error');
    };

    // start image capture
    navigator.device.capture.captureImage(captureSuccess, captureError);
```
****

#### 录制视频
`navigator.device.capture.captureVideo(successCB, failedCB[, options])`

`options` 可选项：

    key | 描述
    ---- | ----
    limit | 拍摄视频的最大数量，默认1（支持Android）
    quality | 视频质量，1：高质量，0：低质量（支持Android）
    
example:

```js
    // capture callback
    var captureSuccess = function(mediaFiles) {
        var i, path, len;
        for (i = 0, len = mediaFiles.length; i < len; i += 1) {
            path = mediaFiles[i].fullPath;
            // do something interesting with the file
            console.log(path);
        }
    };

    // capture error callback
    var captureError = function(error) {
        alert('Error code: ' + error.code, null, 'Capture Error');
    };

    // start video capture
    navigator.device.capture.captureVideo(captureSuccess, captureError);
```
****

#### 录制音频
`navigator.device.capture.captureAudio(successCB, failedCB[, options])`

`options` 可选项：

    key | 描述
    ---- | ----
    limit | 录制音频片段的最大数量，默认1（支持Android）
    
example:

```js
    // capture callback
    var captureSuccess = function(mediaFiles) {
        var i, path, len;
        for (i = 0, len = mediaFiles.length; i < len; i += 1) {
            path = mediaFiles[i].fullPath;
            // do something interesting with the file
            console.log(path);
        }
    };

    // capture error callback
    var captureError = function(error) {
        alert('Error code: ' + error.code, null, 'Capture Error');
    };

    // start audio capture
    navigator.device.capture.captureAudio(captureSuccess, captureError);
```
****


