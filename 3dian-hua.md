# 电话
**模块名称：DialPhone**

## 方法
* [DialPhone.dial](#拨打电话)：拨打电话
* [DialPhone.getAllContacts](#获取通讯录中所有联系人)：获取通讯录中所有联系人
* [DialPhone.showAddressbook](#打开通讯录)：打开通讯录

### 拨打电话
**用法：**`DialPhone.dial("电话号码", successCB, failedCB)`
**示例：**

```js
    DialPhone.dial("10086", function(){
    	console.log('拨号成功');
    },function(errorObj){
    	alert('拨号失败'+ JSON.stringify(errorObj));
    })
```

### 获取通讯录中所有联系人
**用法：**`DialPhone.getAllContacts(successCB, failedCB)`

```js
    //联系人对象
    contactObj = {
        "address":[
            "四川省成都市",
            ...
        ],
        "name":"",
        "phoneNumber":[
            "10086",
            ...
        ]
    }
```

**示例：**

```js
    DialPhone.getAllContacts(function(contactObjList){
    	console.log(JSON.stringify(contactObjList, null, 2));
    },function(errorObj){
    	alert('失败'+ JSON.stringify(errorObj));
    })
```

### 打开通讯录
**用法：**`DialPhone.showAddressbook(successCB, failedCB)`
**示例：**

```js
    DialPhone.showAddressbook(function(contactObj){
    	console.log(JSON.stringify(contactObj, null, 2));
    },function(errorObj){
    	alert('失败'+ JSON.stringify(errorObj));
    })
```

