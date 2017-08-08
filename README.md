# jdi-auto-update-android
auto update for android

## 目录

* [功能介绍](#功能介绍)
* [Gradle 依赖](#Gradle依赖)
* [简单使用](#简单使用)
* [License](#license)

## 功能介绍

- [x] 实现android版本更新
- [x] 支持后台下载
- [x] 支持静默下载（可以设置wifi状态下）
- [x] 支持android7.0

## Gradle 依赖

```gradle
dependencies {
    compile 'com.xulaoyao.android.jdi:autoupdate:0.1.0'
}
```


## 简单使用

```java
	new UpdateAppManager
                .Builder()
                //当前Activity
                .setActivity(this)
                //更新地址
                .setUpdateUrl(mUpdateUrl)
                //实现httpManager接口的对象
                .setHttpManager(new UpdateAppHttpUtil())
                .build()
                .update();
```
 
## 服务端

```json
{
  "versionCode": 2,
  "versionName": "0.2.1",
  "url": "http://www.your-website.com/xxx-100-20170803-03_18_13.apk",
  "msg": "1，添加删除信用卡接口。\r\n2，添加vip认证。\r\n3，区分自定义消费，一个小时不限制。\r\n4，添加放弃任务接口，小时内不生成。\r\n5，消费任务手动生成。",
  "size": "1024",
  "md5":"db2e7e39fe3d5501c9b64fce2865f73d"
}
```


## License

   	Copyright 2017 otnp

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
