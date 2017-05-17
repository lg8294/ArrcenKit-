# 电话
**模块名称：DialPhone**

## 方法
* DialPhone.dial
* DialPhone.getAllContacts
* DialPhone.showAddressbook

### 拨打电话

`DialPhone.dial("电话号码", successCB, failedCB)`

example:

```js
    DialPhone.dial("10086", function(){
    	console.log('拨号成功');
    },function(errorObj){
    	alert('拨号失败'+ JSON.stringify(errorObj));
    })
```

### 获取通讯录
`DialPhone.getAllContacts(successCB, failedCB)`

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

example:

```js
    DialPhone.getAllContacts(function(contactObjList){
    	console.log(JSON.stringify(contactObjList, null, 2));
    },function(errorObj){
    	alert('失败'+ JSON.stringify(errorObj));
    })
```

### 打开通讯录
`DialPhone.showAddressbook(successCB, failedCB)`

example:

```js
    DialPhone.showAddressbook(function(contactObj){
    	console.log(JSON.stringify(contactObj, null, 2));
    },function(errorObj){
    	alert('失败'+ JSON.stringify(errorObj));
    })
```

