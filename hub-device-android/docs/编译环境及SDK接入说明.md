 * [准备开发环境](#准备开发环境)
 * [创建一个新的Android工程](#创建一个新的Android工程)
 * [引用方式](#引用方式)
 * [根据用户业务逻辑开发相关功能](#根据用户业务逻辑开发相关功能)

## 准备开发环境
SDK Demo 示例中使用的是 Android Studio 版本为4.0.1，gradle版本为6.3。
Android Studio 可在 [Android developers 官网](https://developer.android.com/studio)下载，Android 开发教程，请参考 Android developers 官网文档。

## 创建一个新的Android工程

## 引用方式
- 集成 SDK 方式
  若不需要将 IoT-SDK 运行在 service 组件中，则只需要依赖 [iot_core](https://github.com/tencentyun/iot-device-java/tree/master/hub-device-android/iot_core)
 -  依赖 maven 远程构建
    ``` gr
    dependencies {
        implementation 'com.tencent.iot.hub:hub-device-android-core:3.2.0'
        implementation 'com.tencent.iot.hub:hub-device-android-service:3.2.0'
    }
    ```
 -  依赖本地sdk源码 构建
    修改应用模块的 **[build.gradle](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/hub-demo/build.gradle)**，使应用模块依赖 [iot_core](https://github.com/tencentyun/iot-device-java/tree/master/hub-device-android/iot_core) 和[iot_service](https://github.com/tencentyun/iot-device-java/tree/master/hub-device-android/iot_service)源码，示例如下：
     ```gr
    dependencies {
        implementation project(':hub-device-android:iot_core')
        implementation project(':hub-device-android:iot_service')
    }
     ```

## 根据用户业务逻辑开发相关功能
用户调用各个功能API接口可以参考 [hub-device-android示例Demo目录索引.md](https://github.com/tencentyun/iot-device-java/blob/master/hub-device-android/docs/hub-device-android示例Demo目录索引.md) 中对应各个功能示例。
