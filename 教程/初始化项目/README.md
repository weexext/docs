# 项目创建

## 搭建开发环境

### 安装配置 weex 基本开发环境，包括：

- 安装 node 与 npm
- 安装 [weex-toolkit](https://weex.incubator.apache.org/cn/guide/tools/toolkit.html)

具体的安装与配置细节，请参考 [weex中文官网](http://weex-project.io/cn/guide/set-up-env.html)

### 安装 weex-tools
- weex-tools 是基于 weexpack 二次开发而来的 CLI 工具；
- weex-tools 针对 ucar-weex-ext-sdk 进行了一些定制，使得编译打包的过程更为顺畅；
- 关于 weex-tools 更多的信息请参考 weex-tools 对应的 [wiki 条目](https://github.com/weexext/ucar-weex-core/blob/master/wiki/%E9%A1%B9%E7%9B%AE%E5%BC%80%E5%A7%8B/weextools.md)。
- 使用如下命令安装 weextools
  ```
  npm install -g weextools
  ```

### Android & iOS 开发环境
- 除了上述与 weex 相关的开发环境，还需要根据自身的开发需求安装 Android 或者 iOS 相应的开发环境；
- 对于 windows 操作系统中 Android 开发环境的搭建，需要您将 ANDROID_HOME、 adb 等加入环境变量。

## 开始运行demo

  搭建好上述开发环境后，可按照下面的步骤使用 CLI 工具初始化并运行模板项目

  1. 初始化项目：该命令将在当前目录下生成名为 awesome-project 的模板项目，运行命令时项目名称可以自行修改；
  ```
  weextools create awesome-project
  ```
  2. 进入项目目录中，并安装 npm 依赖
  ```
  cd awesome-project
  npm install
  ```
  3. 编译 js：将编写的 .vue 文件编译成 js 文件
  ```
  npm run build
  ```
  4. 编译 Android 包
  ```
  weextools build android
  -------------------------
  //或
  npm run packzip
  
  npm run copy:android
  
  cd patforms/android
  
  gradle build
  
  ```
  5. 安装 apk 包到手机
  ```
  weextools install android
  -------------------------
  或
  cd patforms/android
    
  gradle iD
  
  ```
   
   
