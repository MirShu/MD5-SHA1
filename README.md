# Android获取MD5、SHA1
# 很多的时候都需要获取Android 的 MD5、SHA1 值，像高德、百度地图就是例子需要这个值做密钥。

下面Android studio工具获取方法

### 1、点击 studio面板右上角 Gradle，找到app>Task>android>signingReport，

![2781551-67df8bb6f965342a](https://user-images.githubusercontent.com/13359093/211514577-5d939711-d84c-42fa-b90c-cb6a0ec371c0.png)

### 双击signingReport 就可以看到studio底部的run输出平台就会出现想要的 MD5、SHA1、SHA-256值了

![2781551-1c8acad7cc5d0e21](https://user-images.githubusercontent.com/13359093/211514692-b3c12c51-0cf9-41f8-a3b7-2273fd1f9e95.png)

### 2、 有些时候可能会出现Gradle中没有Tasks情况，

![2781551-0ec15c1da6eeb8f5](https://user-images.githubusercontent.com/13359093/211514783-04cfe414-8a1e-49a6-b0b8-66deb358de7f.png)

解决办法；

# 第一步、studio面板左上角，File > Setting > Experimental

```
 Do not build Gradle task list during Gradle scnc 
```
这一句前面的勾取消掉，然后保存>再点击ok按钮返回


![2781551-44e87f7281ef4d30](https://user-images.githubusercontent.com/13359093/211514962-49713770-0ef5-48cf-a322-ba75d0a791f5.png)

### 第二步、返回到面板再点击 File>Sync Project with Gradle Files 同步下Gradle 文件就可以了，此时打开右上角的Gradle 就会有Task，重复 1 既可以获取MD5、SHA1值

![2781551-21c2069bfe7394ae](https://user-images.githubusercontent.com/13359093/211515104-1d9fd3d5-24d5-4b19-af2f-e71c154e5813.png)
