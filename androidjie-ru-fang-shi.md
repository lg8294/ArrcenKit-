# Android接入方式
## 1.下载ArrcenKit.framework

## 2.创建Android工程

## 3.导入libs
拷贝libs下的文件到工程app/libs目录下，如下图：
![](/image/Android/2.1-1.png)
![](/image/Android/2.0.png)
![](/image/Android/2.2-1.png)
![](/image/Android/2.3-1.png)

## 4.导入jniLibs
拷贝jniLibs文件夹到工程app/src/main目录下，如下图：
![](/image/Android/3.0-1.png)
![](/image/Android/3.1-1.png)
![](/image/Android/3.2-1.png)

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
![](/image/Android/14888549553239.jpg)
![](/image/Android/14888549265926.jpg)

## 配置AndroidManifest.xml
`manifest` 中添加下面的代码：

```xml
<application
    ...
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
    
    <meta-data        android:name="com.baidu.lbsapi.API_KEY"        android:value="Your Key" />    <meta-data        android:name="JPUSH_APPKEY"        android:value="Your Key" />
</application>
```

最终效果如下图：
![](/image/Android/14888548077171.jpg)

## 配置gradle.properites
添加  `android.useDeprecatedNdk=true`
![](/image/Android/14888549936546.jpg)

## 添加配置文件
在 `assets` 中新建 `net.arrcencloud.config.json` 配置文件，并编辑[项目配置项](/xiang-mu-pei-zhi-xiang.md)，如下图：


## 导入www.zip文件
在工程app/main目录下新建assets文件夹：
![](/image/Android/5.1-1.png)
![](/image/Android/5.2-1.png)
![](/image/Android/5.3-1.png)

拷贝www.zip到assets目录下：
![](/image/Android/5.4-1.png)
![](/image/Android/5.5.png)