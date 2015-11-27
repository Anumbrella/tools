##tools——Android常用工具库总结

 
* DataUtils:数据转换类
* DateUtils:时间格式转换集合类
* HttpUtils:Http请求常用方法类
* L:Log日志自定义类
* NetUtils:网络监测类
* ScreenUtils:屏幕测量综合类
* SDCardUtils:手机SDCard处理相关类
* T:Toast自定义类

###DataUtils:


 * int dp2px(Context context,int dpValue) 
 * int px2dp(Context context,int pxValue)


###DateUtils:

 * String getStrTime_ymd_hms(String time) <br/>
   将时间戳转换为“yyyy-MM-dd HH:mm:ss”格式的字符串格式<br/>
   time:秒<br/><br/>   
 * String getStrTime_ymd_hm(String time)
 * String getStrTime_ymd(String time)
 * String getStrTime_y(String time)
 * String getStrTime_md_hms(String time)
 * String getStrTime_md(String time)
 * String getStrTime_hm(String time)
 * String getStrTime_hms(String time)<br/>
 上面几种方法都是根据下划线后面的后缀名获取相应格式的时间格式

 * String getTime_secod()<br/>
 获取当前时间的时间戳(返回值为秒)
 
 * String getTime_timeStamp()<br/>
  获取当前时间的时间戳(返回值为毫秒)
  
 * String getStrTimeSection(String time)<br/>
 将时间戳转换为“yyyy.MM.dd EEEE”格式的字符串格式,”EEEE”代表的是星期几<br/>
 time:秒<br>
 
 

###HttpUtils:

* void doGetAsyn(final String url, final CallBack callBack)
* void doPostAsyn(final String url, final CallBack callBack)
* String doGet(final String url, String params)
* String doPost(final String url, String params)<br/>
Http常用请求


###L:

* void d(String  message)
* void i(String  message)
* void e(String  message)
* void v(String  message)<br/>
以上的方法分别对应Log.d(String tag, String msg),Log.i(String tag, String msg),Log.e(String tag, String msg),Log.v(String tag, String msg)方法
* void d(String tag,String  message)
* void i(String tag,String  message)
* void e(String tag,String  message)
* void v(String tag,String  message)<br/>
可以在方法里自定义TAG,也可以初始化定义TAG

* logRecord(String logPath, String tag, String message)<br/>
将日志信息写入文件当中,默认关闭,使用L.isRecord = true,可以开启日志写入文件中,L.TAG指定自定义TAG,L.APPName指定日志记录文件夹的名称,一般为app的名称


###NetUtils:

* boolean isConnected(Context context)<br/>
手机是否联网<br/>

* boolean isWifi(Context context)<br/>
wifi是否可用<br/>

* int getConnectedType(Context context)<br/>
获取连接网络的类型<br/>


###ScreenUtils:


* int getScreenWidth(Context context) 
* int getScreenHeight(Context context)<br/> 
获取屏幕的宽高<br/>

* int getStatusHeight(Context context)<br/>
获取状态栏的高度

* Bitmap snapShotWithStatusBar(Activity activity)<br/>
获取当前Activity的屏幕截图,包含状态栏的高度

* Bitmap snapShotWithoutStatusBar(Activity activity)<br/>
获取当前Activity的屏幕截图,不包含状态栏的高度 


###SDCardUtils:

* boolean isSDCardEnable()<br/>
获取SDCard是否可用 

* String getSDCardPath()<br/>
获取SDCard的路径
* long getAvaliableSDCardSize()
* long getAllSDCardSize()<br/>
获取SDCard的存储容量情况

* long getFreeBytes(String filePath)<br/>
获取指定路径文件夹下可用的空间大小

* long getRomTotalSize()<br/>
获取手机内存的总容量

* String getRootDirectoryPath()<br/>
获取系统存储路径


###T:

* void showShort(Context context, CharSequence message)
* void showShort(Context context, int message)
* void showLong(Context context, CharSequence message)
* void showLong(Context context, int message)<br/>
不同数据类型Toast长、短时间显示信息
<br/>
<br/>
* void show(Context context, CharSequence message, int duration)
* void show(Context context, int message, int duration)<br/>
不同数据类型的自定义Toast显示



####添加依赖:
```bash
complie 'net.anumbrella:utils:1.0.1'
```

  
####License:

Copyright 2015 Anumbrella

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

  
  
  