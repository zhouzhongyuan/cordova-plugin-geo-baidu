#cordova-plugin-geoloaction-baidu-android
#百度定位SDK cordova插件
##特点
* 返回json格式的数据
* 返回的json数据与cordova-plugin-geolocation一致
* 可与官方插件配合使用，platform为android时使用本插件，iOS时使用官方插件。

##适用对象
* **中国**定位不准确的cordova **Android** 应用程序

##不适用于
* iOS

##安装之前
* API_KEY: 百度定位SDK的key
  * 申请方法请看[申请密钥Android定位SDK](http://developer.baidu.com/map/index.php?title=android-locsdk/guide/key)

##安装
```
cordova plugin add https://github.com/zhouzhongyuan/cordova-plugin-geoloaction-baidu-android --variable API_KEY="<API_KEY>"
**注：API_KEY不带左右尖括号**
```



##以下为引用别人人内容

#百度地图定位Android版插件
本插件利用百度地图提供的定位功能进行Android版手机定位。
  
####为什么没有iOS版？
因为iOS版有官方的定位插件_cordova-plugin-geolocation_可以使用。

请参照：[cordova-plugin-geolocation](https://github.com/apache/cordova-plugin-geolocation)

####Android版为什么不使用官方的_cordova-plugin-geolocation_插件
最新版的插件已经删除掉的Android版定位的代码，改为基于系统浏览器(chrome内核)进行定位。

为什么这样做，也有人问过同样的问题，作者的回答是这样比原生定位更快更准确。

但经过测试后，发现根本无法定位，几经调查发现跟貌似国内网络有关系，原因相信大家都懂的，此过省略好几个字。。。。

__此插件就这么诞生了__

####版本
基于百度地图Android版定位SDK（v5.3）

####一，申请密钥
请参照：[申请密钥Android定位SDK](http://developer.baidu.com/map/index.php?title=android-locsdk/guide/key)

####二，安装插件

```
cordova plugin add https://github.com/zhouzhongyuan/cordova-plugin-geoloaction-baidu-android --variable API_KEY="<API_KEY>"
**注：此处的API_KEY来自于第一步，不带左右尖括号**
```

####三，使用方法

```
// 进行定位
baidu_location.getCurrentPosition(successCallback, failedCallback);
```

获得定位信息，返回JSON格式数据:

```
{
  latitude : 纬度,
  lontitude: 经度,
  ...
}
```
具体字段内容请参照：[BDLocation](http://developer.baidu.com/map/loc_refer/index.html)

####四，查看当前安装了哪些插件

```
cordova plugin ls
```

####五，删除插件

```
cordova plugin rm cordova-plugin-geoloaction-baidu-android
```
#### To do
升级 Baidu android SDK form 5.3 to 6.0







