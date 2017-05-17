# iOS接入方式

## 下载ArrcenKit.framework

## 创建iOS工程

## 导入ArrcenKit.framework
打开工程目录，新建文件夹 `Frameworks` ，复制 `ArrcenKit.framework` 到该文件夹下，效果如下图：
![](/image/iOS/1.0.png)

右键工程目录，选择 `Add Files to "Demo"...` ，在打开的窗口中选择 `Frameworks` 文件夹，点击 `Add` ，效果如下图：
![](/image/iOS/1.1.png)

点击ArrcenKit.framework左侧的箭头，展开ArrcenKit.framework，找到SocketIO.framework，拖动SocketIO.framework到和ArrcenKit.framewrok同一级，如下图：
![](/image/iOS/1.2.png)
![](/image/iOS/1.3.png)
![](/image/iOS/1.4.png)

在TARGETS-General-Embedded Binaries选项，点击 `+` ，选择SocketIO.framework，点击 `Add` 如下图：
![](/image/iOS/1.5.png)
![](/image/iOS/1.6.png)
![](/image/iOS/1.7.png)

## 导入cordova
右键工程目录，选择 `Add Files to "Demo"...` ，在打开的窗口中选择 `Frameworks/ArrcenKit.framework/cordova` 文件夹，点击 `Option` 选项，`Added folders` 选择 `Create folder references` ，点击 `Add` ，效果如下图：
![](/image/iOS/2.0.png)
![](/image/iOS/2.1.png)

## 导入Resources
右键工程目录，选择`Add Files to "Demo"...` ，在打开的窗口中选择 `Frameworks/ArrcenKit.framework/Resources` 文件夹，点击 `Option` 选项，`Added folders` 选择 `Create groups` ，点击 `Add` ，如下图：
![](/image/iOS/3.0.png)
![](/image/iOS/3.1.png)

## 导入工程xcconfig配置文件
右键工程目录，选择`Add Files to "Demo"...` ，在打开的窗口中选择 `Frameworks/ArrcenKit.framework/Config` 文件夹，如下图：
![](/image/iOS/4.0.png)
![](/image/iOS/4.1.png)

打开PROJECT-Demo-Info选项，配置Configurations，如下图：
![](/image/iOS/4.2.png)

## 修改main.m文件
打开 Demo-Supporting Files-main.m 文件，修改引入的头文件和代码，如下图：
![](/image/iOS/5.0.png)
![](/image/iOS/5.1.png)

代码如下：

```js
#import <UIKit/UIKit.h>
#import <ArrcenKit/ArrcenKit.h>

int main(int argc, char * argv[]) {
    @autoreleasepool {
        return UIApplicationMain(argc, argv, nil, NSStringFromClass([ArrcenAppDelegate class]));
    }
}
```

## 添加项目配置文件
选择Demo目录，新建文件 `net.arrcencloud.config.json` ，并编辑[项目配置项](/xiang-mu-pei-zhi-xiang.md)，如下图：
![](/image/iOS/6.1.png)
![](/image/iOS/6.2.png)
![](/image/iOS/6.3.png)

## 修改用户权限和第三方APP回调

## 添加www.zip文件