# Android接入方式
## 下载ArrcenKit.framework

## 创建Android工程

## 导入libs
拷贝 `libs` 下的文件到工程 `app/libs` 目录下，如下图：
![](/image/Android/2.1.png)
![](/image/Android/2.2.png)

## 导入jniLibs
拷贝 `jniLibs` 文件夹到工程 `app/src/main` 目录下，如下图：
![](/image/Android/3.0.png)
![](/image/Android/3.1.png)

## 导入wxapi
拷贝 `wxapi` 文件夹到工程 `app/src/main/java/{包名}` 目录下，如下图：
![](/image/Android/9.1.png)
![](/image/Android/9.0.png)
![](/image/Android/9.2.png)

## 配置app下的build.gradle
添加

```
    repositories {
        flatDir {
            dirs 'libs'
        }
    }
```

`defaultConfig` 下添加：

```
    ndk {//海康sdk只支持32位
        abiFilters "armeabi-v7a","armeabi"
    }
```

`dependencies` 中添加以下代码：

```
    compile(name: 'CordovaLib-release', ext: 'aar')
    compile(name: 'Framework-release', ext: 'aar')
    compile(name: 'Barcodescanner-release', ext: 'aar')
    compile 'com.google.code.gson:gson:2.7'
    compile 'com.zhy:okhttputils:2.6.2'
    compile('io.socket:socket.io-client:0.7.0') {
        // excluding org.json which is provided by Android
        exclude group: 'org.json', module: 'json'
    }
```

最终效果如下图：
![](/image/Android/4.0.png)
![](/image/Android/4.1.png)

## 修改AndroidManifest.xml
用下面的代码覆盖 `activity` ：
```xml
    <activity
        android:name="com.arrcen.framework.ui.StartActivity"
        android:launchMode="singleTop"
        android:screenOrientation="portrait"
        android:theme="@android:style/Theme.DeviceDefault.NoActionBar">
        <intent-filter>
            <action android:name="android.intent.action.MAIN" />
            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>
    </activity>
    
    <activity
        android:name="com.tencent.tauth.AuthActivity"
        android:launchMode="singleTask"
        android:noHistory="true">
        <intent-filter>
            <action android:name="android.intent.action.VIEW" />
            
            <category android:name="android.intent.category.DEFAULT" />
            <category android:name="android.intent.category.BROWSABLE" />
            
            <data android:scheme="tencent1106031424" />
        </intent-filter>
    </activity>
```

在 `application` 中添加以下代码：

```xml
    <meta-data
        android:name="com.baidu.lbsapi.API_KEY"
        android:value="Your Key" />
    <meta-data
        android:name="JPUSH_APPKEY"
        android:value="Your Key" />
```

最终效果如下图：
![](/image/Android/5.0.png)
![](/image/Android/5.1.png)

## 配置gradle.properites
添加  `android.useDeprecatedNdk=true`
![](/image/Android/6.0.png)

## 添加项目配置文件
在工程 `app/main` 目录下新建 `assets` 文件夹：
![](/image/Android/7.0.png)
![](/image/Android/7.1.png)

然后在 `assets` 中新建 `net.arrcencloud.config.json` 配置文件，并编辑[项目配置项](/xiang-mu-pei-zhi-xiang.md)，如下图：
![](/image/Android/8.0.png)
![](/image/Android/8.1.png)

## 导入www.zip文件
拷贝www.zip到 `assets` 目录下。