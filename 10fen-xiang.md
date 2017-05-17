# 分享
**模块名称：Share**

****

### 消息对象

****

## 方法
* Share.send

### 发送分享
`Share.send(type,msgObj,successCB,failedCB)`

`type` 可选项：

* Share.ServiceType.QQ
* Share.ServiceType.Sinaweibo
* Share.ServiceType.Weichat

example:

```js
	var message = {
		"content" : "内容",//(String 类型 )分享消息的文字内容
		"thumbs" : [],//(Array[ Stromg ] 类型 )分享消息的缩略图,分享消息中包含的缩略图路径； 若分享平台仅支持提交一张图片，传入多张图片则仅提交第一张图片； 如果分享平台的信息不支持缩略图，若没有设置消息的图片（pictures）则使用缩略图，否则忽略其属性值。 注意：图片有大小限制，推荐图片小于20Kb。
		"pictures" : [],//(Array[ String ] 类型 )分享消息的图片,分享消息中包含的图片路径，仅支持本地路径。 若分享平台仅支持提交一张图片，传入多张图片则仅提交第一张图片。 如果不能同时支持其它内容信息，优先级顺序为：pictures>content。
		"href" : "",//(String 类型 )分享独立的链接,分享独立链接地址，仅支持网络地址（以http://或https://开头）。 如果不能同时支持其它内容信息，优先级顺序为：href>pictures>content。

		"title" : "标题",//(String 类型 )分享消息的标题,目前仅微信分享独立链接消息时支持。
		"extra" : {},//(ShareMessageExtra 类型 )分享消息扩展参数
		"geo" : {//(GeoPosition 类型 )分享消息中包含的用户地理信息数据
			"latitude" : 0,
			"longitude" : 0
		},
		"interface" : "auto"//(String 类型 )分享消息的模式,可取值： "auto" - 自动选择，如果已经安装微博客户端则采用编辑界面进行分享，否则采用无界面分享； "slient" - 静默分享，采用无界面模式进行分享； "editable" - 进入编辑界面，用户确认分享内容后发送，如果当前未安装微博客户端则触发错误回调。 默认值为"auto"。 （仅新浪微博分享时生效）
	};
	Share.send(Share.ServiceType.Sinaweibo,message,function (successObj) {
		console.log(JSON.stringify(successObj, null, 2));
	}, function (error) {
		alert(JSON.stringify(error));
	});
```

****

