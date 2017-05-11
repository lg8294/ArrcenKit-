## 8.消息提醒
**模块名称：==Setting==**

```js
// 提醒音对象
soundObj = {
   id:"",// id
   name:"",// 名称
   dis:""// 描述
}
```

****

#### 方法
* Setting.getMessageAlertSoundList
* Setting.setSoundAlert
* Setting.setVibrateAlert
* Setting.setMessageAlertSound
* Setting.playSound

#### 获取消息提醒声音列表
`Setting.getMessageAlertSoundList(successCB, failedCB)`
    
```js
    //成功对象
    successObj = {
       list:[
           soundObj,
           ...
       ],//消息提醒音列表
       sound:true,//声音是否打开
       vibrate:true,//震动是否打开
       used:soundObj//正在使用的消息提醒音
    }
```

example:

```js
	Setting.getMessageAlertSoundList(function(successObj){
		console.log('获取声音列表 成功\n' + JSON.stringify(successObj, null, 2));
	}, function (errorObj) {
	   console.log(JSON.stringify(errorObj);
	});
```

****

#### 设置声音提醒是否打开
`Setting.setSoundAlert(enable, successCB, errorCB)`

`enable` 可选项：

* true：打开声音提醒
* false：关闭声音提醒

example:

```js
	Setting.setSoundAlert(true, function(){
		console.log('成功');
	}, function (error) {
		console.log("失败");
	});
```

****

### 设置震动是否打开
`Setting.setVibrateAlert(enable, successCB, errorCB)`

`enable` 可选项：

* true：打开震动提醒
* false：关闭震动提醒

example:

```js
	Setting.setVibrateAlert(true, function(){
		console.log('成功');
	}, function (error) {
		console.log("失败");
	});
```

****

### 设置消息提醒声音
`Setting.setMessageAlertSound(soundObj, successCB, errorCB)`

example:

```js
    Setting.setMessageAlertSound(soundObj, function(){
        console.log('成功');
    }, function (error) {
        console.log("失败");
    });
```

### 播放提醒音
`Setting.playSound(soundObj)`

example:

```js
    Setting.playSound(soundObj);
```

****

