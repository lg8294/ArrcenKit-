# 条码、二维码
**模块名称：==BarcodeScanner==**
[ngcordova](http://ngcordova.com/docs/plugins/barcodeScanner/)
[使用说明](https://github.com/phonegap/phonegap-plugin-barcodescanner)

****

## 方法
* BarcodeScanner.scan
* BarcodeScanner.encode

****

## 扫码
`BarcodeScanner.scan(successCB, failedCB[, options])`

`options` 可选项：

    key | 描述
    --- | ---
    preferFrontCamera | 布尔值，是否用前置摄像头
    showFlipCameraButton | 布尔值，显示。。。。
    showTorchButton | 布尔值，显示。。。。
    torchOn | 布尔值，加载的时候打开。。。。（支持Android）
    prompt | 提示。。。。（支持Android）
    resultDisplayDuration | 多少ms后显示结果，默认1500ms(支持Android）
    formats | 支持扫描条码的类型，默认所有类型，除了PDF_417和RSS_EXPANDED
    orientation | 方向，默认跟随设备方向（支持Android）
    disableAnimations | 布尔值，禁用动画（支持iOS）
    disableSuccessBeep | 布尔值，禁用成功后响声（支持iOS）
    
example:

```js
    BarcodeScanner.scan(function (result) {
        alert("We got a barcode\n" + "Result: " + result.text + "\n" + "Format: " + result.format + "\n" + "Cancelled: " + result.cancelled);
    }, function (error) {
        alert("Scanning failed: " + error);
    }, {
        "preferFrontCamera" : true, // iOS and Android
        "showFlipCameraButton" : true, // iOS and Android
        "prompt" : "Place a barcode inside the scan area", // supported on Android only
        //"formats" : "QR_CODE,PDF_417", // default: all but PDF_417 and RSS_EXPANDED
        "orientation" : "landscape" // Android only (portrait|landscape), default unset so it rotates with the device
    });
```

****

## 生成
`BarcodeScanner.encode(type, data, successCB, failedCB[, options])`

`type` 可选项：

* BarcodeScanner.Encode.TEXT_TYPE
* BarcodeScanner.Encode.EMAIL_TYPE
* BarcodeScanner.Encode.PHONE_TYPE
* BarcodeScanner.Encode.SMS_TYPE

`options` 可选项：

    key | 描述
    ---- | ----
    codeType | 指定生成 _*条形码*_ 还是 _*二维码*_ ，0：二维码，1：条形码，默认 _*二维码*_
    width | 条形码宽度，默认300px
    hight | 条形码高度，默认50px

example:

```js
    BarcodeScanner.encode(BarcodeScanner.Encode.TEXT_TYPE, "http://www.nytimes.com", function(success) {
        alert("encode success: " + success);
    }, function(fail) {
        alert("encoding failed: " + fail);
    }，{
        "codeType":1
    });
```


