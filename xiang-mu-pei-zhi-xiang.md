#项目配置项
键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"DefaultAccount"|String|空|默认账号|自定义
"ClientId"|String|空|Arrcen APPID，业务服务器提供|自定义
"RedirectUrl"|String|空|登录验证回调地址，业务服务器提供|自定义
"UserCenterUrl"|String|空|用户中心地址|正式环境：http://ouc.arrcencloud.net<br />开发环境：http://ouc.eaicz.com
"ProductCategory"|Number|0|产品类别|0：患者服务<br>1：决策支持<br>2：移动医生<br>3：移动护士
"VerificationMode"|Number|0|登录注册模式|0：验证码登录注册<br>1：密码登录注册|
"IM"|Object|空|[IM配置项](#im)|
"Web"|Object|空|[Web配置项](#web)|
"UI"|Object|空|[UI配置项](#ui)|
"Map"|Object|空|[Map配置项](#map)|
"QQ"|Object|空|[QQ配置项](#qq)|
"Wechat"|Object|空|[微信配置项](#wechat)|
"Weibo"|Object|空|[新浪微博配置项](#weibo)|

<span id="im">`IM` 配置项：<span />

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"Url"|String|空|IM服务地址|正式环境：http://im.arrcencloud.net:7080<br />开发环境：http://eaicz.com:7080
"Project"|String|空|IM中传的项目名|目前统一使用项目包名

<span id="web">`Web` 配置项：<span />

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"BusinessUrl"|String|空|业务中心地址|自定义
"GuidePath"|String|空|引导页配置文件路径，指在www文件夹中的绝对路径，如：/www/loadpage|自定义
"UserAgreementPath"|String|空|用户协议路径，指在www文件夹中的绝对路径，如：/www/user-agreement/user-agreement.html|自定义
"DefaultVersion"|String|空|默认www版本|自定义

`UI` 配置项：

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"ThemeColor"|String||主题色
"KeyDownColor"|按键按下去的颜色
"ProductLogo"|产品Logo
"ProductEnName"|产品英文名
"ProductCnName"|产品中文名
"Copyright"|版权信息
"StartPage"|启动页（Android）
"UpdatePageStartColor"|更新页渐变色开始值
"UpdatePageEndColor"|更新页渐变色结束值
"ProgressBackgroundColor"|更新页进度块未更新区域颜色

`Map` 配置项：

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"BaiduApiKey"|百度地图AppKey


`QQ` 配置项：

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"QQ":"AppId"|QQSDK AppID

`Wechat` 配置项：

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"Wechat":"AppId"|微信SDK AppID
"Wechat":"AppSecret"|微信SDK AppSecret

`Weibo` 配置项：

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"Weibo":"AppKey"|微信SDK AppKey
"Weibo":"AppSecret"|微信SDK AppSecret
"Weibo":"RedirectUrl"|微信SDK 授权回调地址


```json
{
  "DefaultAccount": "",
  
  "ClientId": "",
  "RedirectUrl": "",
  
  "UserCenterUrl": "",
  "IM": {
    "Url": "",
    "Project": ""
  },
  
  "Web": {
    "BusinessUrl": "",
    "GuidePath": "www/loadpage",
    "UserAgreementPath": "/www/user-agreement/user-agreement.html",
    "DefaultVersion":"1.0"
  },
  
  "ProductCategory": 0,
  "VerificationMode": 0,
  "UI": {
    "ThemeColor": "",
    "KeyDownColor": "",
    "ProductLogo": "",
    "ProductEnName": "",
    "ProductCnName": "",
    "Copyright": "",
    "StartPage": "",
    "UpdatePageTopColor": "",
    "UpdatePageBottomColor": "",
    "UpdateProgressBackgroundColor": ""
  },
  "Map": {
    "BaiduApiKey": ""
  },
  "QQ": {
    "AppId": ""
  },
  "Wechat": {
    "AppId": "",
    "AppSecret":""
  },
  "Weibo": {
    "AppKey": "",
    "AppSecret": "",
    "RedirectUrl": ""
  }
}
```

