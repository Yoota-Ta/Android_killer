##  说明

主要是工具版本有点老，对相关的依赖进行了升级，目前测试逆向，功能正常

## 鸣谢

- [APK2AAB](https://github.com/sensei-z/APK2AAB)

- [AndroidKiller](https://github.com/liaojack8/AndroidKiller)



------



### apk下载

```
https://apkcombo.com/
https://apkpure.com/
```

### 需要

```
去除:
<meta-data android:name="com.android.vending.derived.apk.id" android:value="1"/>

<uses-permission android:name="android.permission.REQUEST_INSTALL_PACKAGES" />



添加:
android:exported="false" 
android:exported="true"


功能最好隐藏 不要删除:
android:visibility="gone" 


android:visible="false"

<menu xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:id="@+id/action_search"
          android:title="@string/search_title"
          android:icon="@drawable/ic_search"
          android:showAsAction="always"
          android:visible="false" />
</menu>

```

### app icon 

```
下载icon
https://jiejingku.net/icon/index.html

https://www.flaticon.com/search?word=note&color=color

图标工厂：
https://icon.wuruihong.com/

```

### 修改包名

更改AndroidManifest.xml里面的包名

```
1.修改 <manifest>标签里的 package
2.全局更改com.xxx.xxxx类似的包名 
3.全局更改smali类型代码的包名字符串  Lcom/xxx/xxxx      
4.全局更改所有com/xxx/xxxx文件夹的名称，因为java文件里面要求包名和文件夹路径要对应

com.zczc.wallify
com.hdw.lovewallpapers

Lcom/hdw/lovewallpapers
Lcom/zczc/wallify

修改文件夹名，包名用小写字母

修改应用名
```



### apk转aab

```
 工具
 https://github.com/sensei-z/APK2AAB
 
 *** 安装 路径不要有中文,apk包放在工具路径下，都不要中文,路径以及名称不能有空格
 
 
 https://github.com/37sy/build_aab_tool
 
```

* 注意这里需要jdk1.8，版本不能高 

```
因为逆向需要JDk1.8
JAVA_HOME=D:\Program Files\Java\jdk1.8.0_341

Android的开发用的jdk20
JAVA_HOME=D:\Android\sdk_adr
```

### 生成jks 证书

```
keytool -genkey -alias ali -keyalg RSA  -keysize 2048 -validity 36500 -keystore jks.jks

```



### aab签名

```
工具
https://www.fair-guard.com/help/list-228.html

java -jar FairGuard4.2.8.jar -optype_sign_jar -inputfile   %inputfile.aab%  
[-outputfile %output.aab%

说明：
-outputfile 可选项，输出文件路径名。如未设置此选项，则输出文件路径默认为% inputfile.aab %同目录，命名为
以%inputfile_signed.aab %为结尾的文件名


签名信息在 config.ini 文件中配置如下：
[gamekey]
key=
[signinfo]
keystore-path=E:\androidPrj\jks\Test001.jks
alias=ali
password=sqa123456
alias-pwd=sqa123456

```

* 注意ini配置文件的jks路径同上 不能有汉字 空格

### aab转apk

```
bundletool:
https://github.com/google/bundletool/releases

java -jar bundletool-all-1.14.0.jar build-apks 
--bundle=xxx.aab 
--output=xxx.apks 
--ks=xxxx.jks 
--ks-pass=pass:sqa123456 
--ks-key-alias=ali 
--key-pass=pass:sqa123456

```

### 测试aab 

```
apks 解压后有一个跟原来大小一致的apk，安装测试即可
```





### 隐私协议地址

```
https://sites.google.com/

发布：填入名字 
复制链接
https://sites.google.com/view/lovewallify/%E9%A6%96%E9%A1%B5



```



### 需要素材

```
512*512        icon
1024*500       置顶大图
320~3840像素   2 到 8 张手机屏幕截图
```



### google store 切换语言

```
https://myaccount.google.com/language?continue=https%3A%2F%2Fmyaccount.google.com%2Fsecurity%3Fpmr%3D1
```

![](./img/016.png)

### google play

```
https://play.google.com/console/u/0/developers/6485965189370576455/app-list
```

