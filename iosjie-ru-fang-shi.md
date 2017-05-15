# 如何接入ArrcenKit

## iOS接入方式

### 1.下载ArrcenKit.framework

### 2.创建iOS工程

### 3.导入ArrcenKit.framework
向工程目录中拖入ArrcenKit.framework，效果如下图：
![](/image/2-2.png)

点击ArrcenKit.framework左侧的箭头，展开ArrcenKit.framework，找到SocketIO.framework，拖动SocketIO.framework到和ArrcenKit.framewrok同一级，如下图：
![](/image/2.1.png)
![](/image/2.2.png)
![](/image/2.3.png)

在TARGETS-General-Embedded Binaries选项，点击 `+` ，选择SocketIO.framework，点击 `Add` 如下图：
![](/image/2.4.png)
![](/image/2.5.png)
![](/image/2.6.png)

### 4.导入cordova
右键工程目录，选择 `Add Files to "Demo"...` ，在打开的窗口中选择 `ArrcenKit.framework/cordova` 文件夹，如下图：
![](/image/3.0.png)
![](/image/3.1.png)
![](/image/3.2.png)

### 5.导入Resources
右键工程目录，选择`Add Files to "Demo"...` ，在打开的窗口中选择 `ArrcenKit.framework/Resources` 文件夹，如下图：
![](/image/4.0.png)
![](/image/4.1-2.png)

### 6.导入工程xcconfig配置文件
右键工程目录，选择`Add Files to "Demo"...` ，在打开的窗口中选择 `ArrcenKit.framework/Config` 文件夹，如下图：

打开PROJECT-Demo-Info选项，配置Configurations，如下图：

### 7.添加配置文件

### 8.修改main.c文件
