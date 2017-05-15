# 项目配置项
键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"DefaultAccount"|String|空|默认账号|自定义
"ClientId"|String|空|Arrcen APPID，业务服务器提供|自定义
"RedirectUrl"|String|空|登录验证回调地址，业务服务器提供|自定义
"UserCenterUrl"|String|空|用户中心地址|正式环境：http://ouc.arrcencloud.net<br />开发环境：http://ouc.eaicz.com
"ProductCategory"|Number|0|产品类别|0：患者服务<br>1：决策支持<br>2：移动医生<br>3：移动护士
"VerificationMode"|Number|0|登录注册模式|0：验证码登录注册<br>1：密码登录注册|
"IM"|Object|空|[IM配置项](#im)||
"Web"|Object|空|[Web配置项](#web)||
"UI"|Object|空|[UI配置项](#ui)||
"Map"|Object|空|[Map配置项](#map)||
"QQ"|Object|空|[QQ配置项](#qq)||
"Wechat"|Object|空|[微信配置项](#wechat)||
"Weibo"|Object|空|[新浪微博配置项](#weibo)||

## <span id="im">`IM` 配置项：<span />

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"Url"|String|空|IM服务地址|正式环境：http://im.arrcencloud.net:7080<br />开发环境：http://eaicz.com:7080
"Project"|String|空|IM中传的项目名|目前统一使用项目包名

## <span id="web">**`Web` 配置项：**<span />

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"BusinessUrl"|String|空|业务中心地址|自定义
"GuidePath"|String|空|引导页配置文件路径，指在www文件夹中的绝对路径，如：/www/loadpage|自定义
"UserAgreementPath"|String|空|用户协议路径，指在www文件夹中的绝对路径，如：/www/user-agreement/user-agreement.html|自定义
"DefaultVersion"|String|空|默认www版本|自定义

## <span id="ui">`UI` 配置项：<span />

键 | 类型 | 默认值 | 描述 | 值
----|----|----|----|----
"ThemeColor"|String|由产品类别确定|主题色|自定义
"KeyDownColor"|String|由产品类别确定|按键按下去的颜色|自定义
"ProductLogo"|String|由产品类别确定|登录页面产品Logo图片名|自定义
"ProductEnName"|String|由产品类别确定|登录页面产品英文名|自定义
"ProductCnName"|String|由产品类别确定|登录页面产品中文名|自定义
"Copyright"|String||版权信息|自定义
"StartPage"|String||启动页（Android有效）|自定义
"UpdatePageStartColor"|String|由产品类别确定|更新页渐变色开始值|自定义
"UpdatePageEndColor"|String|由产品类别确定|更新页渐变色结束值|自定义
"ProgressBackgroundColor"|String|由产品类别确定|更新页进度块未更新区域颜色|自定义

## <span id="map">`Map` 配置项：<span />

键 | 类型 | 默认值 | 描述 
----|----|----|----
"BaiduApiKey"|String|空|百度地图AppKey

## <span id="qq">`QQ` 配置项：<span />

键 | 类型 | 默认值 | 描述
----|----|----|----
"AppId"|String|空|QQSDK AppID

## <span id="wechat">`Wechat` 配置项：<span />

键 | 类型 | 默认值 | 描述
----|----|----|----
"AppId"|String|空|微信SDK AppID
"AppSecret"|String|空|微信SDK AppSecret

## <span id="weibo">`Weibo` 配置项：<span />

键 | 类型 | 默认值 | 描述
----|----|----|----
"AppKey"|String|空|微信SDK AppKey
"AppSecret"|String|空|微信SDK AppSecret
"RedirectUrl"|String|空|微信SDK 授权回调地址

## 示例代码
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


