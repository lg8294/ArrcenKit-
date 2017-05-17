# 位置
**模块名称：BaiduMap**

## 方法

* [BaiduMap.getLocation](#获取当前位置)：获取当前位置
* [BaiduMap.getNearList](#获取附近POI列表)：获取附近POI列表
* [BaiduMap.getDistrict](#获取区县位置)：获取区县位置
* [BaiduMap.selectLocation](#选择位置)：选择位置

### 获取当前位置
**说明：**误差控制在10米内。
**用法：**`BaiduMap.getLocation(successCB, failedCB)`

```js
    // 位置信息对象
    // country          国家
    // province         省名
    // city	            城市名
    // district         区县名
    // street           街道名
    // street_number    街道门牌号
    // adcode           行政区划代码
    // country_code     国家代码
    // direction        和当前坐标点的方向，当有门牌号的时候返回数据
    // distance         和当前坐标点的距离，当有门牌号的时候返回数据
    //	var locationObject = {
    //		"location" : {
    //			"lat" : 30.54336890687904,
    //			"lng" : 104.075483
    //		},
    //		formatted_address:'结构化地址信息',
    //			"addressComponent" : {
    //			"adcode" : "510107",
    //			"city" : "成都市",
    //			"country" : "中国",
    //			"country_code" : 0,
    //			"direction" : "",
    //			"distance" : "",
    //			"district" : "武侯区",
    //			"province" : "四川省",
    //			"street" : "天府大道中段辅路",
    //			"street_number" : ""
    //		}
    //	}
```

**示例：**

```js
    BaiduMap.getLocation(function(locationObj){
    	console.log(JSON.stringify(locationObj, null, 2));
    },function (errorObj) {
    	alert(JSON.stringify(errorObj));
    });
```

### 获取附近POI列表
**用法：**`BaiduMap.getNearList(successCB, failedCB)`

```js
    // POI对象
    // addr	地址信息
    // distance	离坐标点距离
    // poiType	poi类型，如’ 办公大厦,商务大厦’
    // location	poi坐标{lat,lng}
    // tel	电话
    // name	poi名称
    // uid	poi唯一标识
    // direction	和当前坐标点的方向
    // cp	数据来源
    // zip	邮编
    
    //	var poiObject = {
    //		"addr" : "天府大道中段1366",
    //		"cp" : " ",
    //		"direction" : "东",
    //		"distance" : "61",
    //		"name" : "天府软件园e6-1",
    //		"poiType" : "公司企业",
    //		"location" : {
    //			"lat" : 104.0749365344204,
    //			"lng" : 30.54342829533655
    //		},
    //		"tag" : "公司企业;园区",
    //		"tel" : "",
    //		"uid" : "47b0d52a4f445e6eb35c6a97",
    //		"zip" : ""
    //	}
```
**示例：**

```js
    BaiduMap.getNearList(function(object){
    	console.log(JSON.stringify(object, null, 2));
    },function (error) {
    	alert(JSON.stringify(error));
    });
```

### 获取区县位置
**说明：**粗略的获取大致位置，对精度不做要求。
**用法：**`BaiduMap.getDistrict(successCB, failedCB)`
**示例：**

```js
    BaiduMap.getDistrict(function(locationObj) {
    	console.log(JSON.stringify(locationObj, null, 2));
    },function (error) {
    	alert(JSON.stringify(error));
    });
```

### 选择位置
**用法：**`BaiduMap.selectLocation(options ,successCB, failedCB)`
**参数：**
`options` 可选项：

    key | type | 默认值 | 描述
    ----- | ----- | ----- | -----
    width | Number | 300 | 图片宽度，单位px
    height| Number | 200 | 图片高度，单位px

**示例：**

```js
    BaiduMap.selectLocation({
    	"width":100,
    	"height":50
    },function(object){
    	console.log(JSON.stringify(object, null, 2));
    },function (error) {
    	alert(JSON.stringify(error));
    });
```

