# 近期网站加了防盗链，建议大家去https://toalan.com/archives/36/ 看原教程，近期会修复



![](https://cos.toalan.com/alan_image/70213dbdab22486697a4a137a9e47176.png)
# 🎈前言（不读前言，会错失很多重要信息）
---

<font color="#86cc00">👑高效远程安装，享受一对一问题解答（远程需要电脑）</font>
- V❤：`cmalin66` 
- Telegram：[Click Me](https://t.me/AlanChen365)
---
不远程？💬有问题？该系列教程官方交流群你值得拥有。Q群：`552158932` 


If you happen to come across this GitHub repository, we warmly welcome your visit. However, we advise you to check your system version before proceeding. If your phone was released before May 15, 2019, which you can verify on websites such as GSMArena, you can install native Google GMS support like a regular Android device, and therefore, you won't need this tutorial.

This tutorial for installing a native GMS solution ('原生谷歌三件套') is only applicable to Huawei phones running Harmony OS, which includes almost all Huawei phones intended for sale in Mainland China. It is not for Huawei phones running on EMUI or any Huawei tablets, except for the Huawei MatePad Pro 10.8 2019 version sold in Mainland China. However, you may still use the MicroG+Play solution listed in the table below.




**华为/荣耀 鸿蒙系统如何安装谷歌框架三件套？恭喜你找对了教程，呕心沥血3个月，终于做出如此完美的教程。**

>🔍[查询支持的型号列表](https://toalan.com/archives/46/)


| 功能\方法                                       | [microG+Play商店](https://toalan.com/archives/123/) | [原生谷歌三件套](https://toalan.com/archives/36/) |
| ------------------------------------------- | ------------------------------------------------- | ------------------------------------------ |
| <font color="#00b050">解决认证弹窗</font>         | 🟢                                                | 🟢                                         |
| 正常使用GMS应用                                   | 🟢                                                | 🟢                                         |
| 应用分身                                        | 🟢                                                | 🟢                                         |
| <font color="#00b050">ChatGPT</font>        | ⛔️                                                | 🟢                                         |
| 更新系统（不要更新5.0）                               | 🟢                                                | 🟢                                         |
| 稳定程度                                        | 🟢                                                | 🟢                                         |
| 更新Google Play 商店                            | 🟢                                                | 🟢                                         |
| 更新Google Play 服务                            | ⛔️（无法使用）                                          | 🟢                                         |
| 玩谷歌游戏                                       | 🟢                                                | 🟢                                         |
| 谷歌Passkey密码填充                               | ⛔️                                                | 🟢                                         |
| <font color="#00b050">GMS消息后台推送(FCM)</font> | 🟢                                                | 🟢                                         |
| 登录提示验证                                      | ⛔️                                                | 🟢                                         |
| 附近分享                                        | ⛔️                                                | 🟢                                         |
| 继续添加谷歌账号                                    | 🟢                                                | ⛔️                                         |
| Google location services                    | 🟢                                                | ⛔️                                         |
| 谷歌企业服务                                      | ❔                                                 | ⛔️                                         |
| GooglePay（需root）                            | ⛔️                                                | ⛔️                                         |
| 查找设备                                        | ⛔️                                                | ⛔️                                         |
>注：🟢全支持、⛔️不支持、❔未测试
>
>FCM消息推送，是一个非常重要的功能，比如你使用 `Wechat` `WhatsApp` `Telegram` 等即时通讯类软件，如果不是在后台运行，就不会有消息通知。
> 如果锁屏和清理了后台，就会错过很多消息。为了解决这个问题，谷歌有GMS在后台运行，华为有HMS。
> 总之就是，它作为中间服务器，如果收到了消息，再拉起应用。这样可以大幅度降低应用一直在后台所带来的电量损耗，还不会错过重要消息。



该教程会不断有优化，简化流程和解决问题。教程永远**免费**并持续更新，有任何问题欢迎评论交流。

- 感谢[xiaohan17]([xiaohan17-一个致力于资源分享的网站](https://xiaohan17.cn/))大佬整理的工具和教程。
- 感谢库安用户`ITMan_CHINA` `蓝夜深空` `leisurefire`  的经验分享。
- 感谢B站UP[晨钟酱Official](https://space.bilibili.com/251013709)提供的ADB工具箱。

# ✔下载链接
---
- [（国内）123网盘下载](https://www.123pan.com/s/x9tA-OClW3.html)
- [（国外）OneDrive网盘下载](https://1drv.ms/u/s!Atp0UM8FnZB_j5lXeIY0H_nE3pHWhQ?e=u3aEAS)

文件结构：
```
华为荣耀鸿蒙完美安装GMS框架开启FCM（手机+电脑+进阶版）
├─Backup
├─GMS手机端安装软件
│  ├─第五步
│  ├─第六步
└─ └─第八步
```

# ✅安装教程（根据反馈不断优化中）
---
> <font color="#ff0000">无论是装过我的教程还是别的教程，装备工作和清理一定要做好。</font>
> <font color="#f79646">⚠注意！该教程需要电脑辅助，如果没有电脑，无法使用最新版Google服务。</font>
> tps：微信分身记得关闭，推荐使用电脑登录备份，后续迁移回来。
## 0. 安装前准备

>**注意:网络需要可以访问[谷歌](https://Google.com)的环境!!!**

1. `设置` - `系统和更新` - `系统导航方式` - `更多` - `悬浮导航` :关闭悬浮导航
2. `设置` - `系统和更新` - `纯净模式` :关闭增强防护
3. `设置` - `隐私` - `隐私空间` :关闭隐私空间
4. `设置` - `应用和服务` - `应用分身` :关闭应用分身
5. `设置` - `电池` - `省电模式`:关闭省电模式

**解压压缩包,将Backup文件夹复制到手机存储空间里的/Huawei 的目录里,压缩包里目录里的软件对应接下来的步骤,按步骤安装!**

>🚨注意！好多人这里没有复制对位置（会导致没有从内部恢复），内部存储是根目录，要复制到 `Huawei` 这个目录下，一般都是有 `huawei` 这个目录的，没有的话自己创建一个。
>正确截图：![正确路径](https://cos.toalan.com/alan_image/4ff00175dce244bfa6a405d3e66b84fa.png)

## 1. 清除谷歌应用数据

-   Google Play商店
-   Google通讯录同步
-   Google Play服务  
-   Google服务框架 
-   Google账户管理程序
-   com.google.android.gms.policy\_sidecar\_aps
-   SharedLibrary
-   谷歌服务助手

	打开 `设置` - `应用和服务` - `应用管理`点击右上角四个点，点击 `显示系统程序`，然后搜索手机里是否有以上软件，若有则卸载。

## 2. 修改系统时间到2019年

`设置` - `系统和更新` - `日期和时间`

将 `自动设置` 关闭，并修改日期到 `2019` 年

## 3. 打开备份,从内部存储恢复

`设置` - `系统和更新` - `备份和恢复`

右上角四个点选择 `从内部存储恢复` ,选择 `toalan.com` 备份,输入密码 `a12345678` 恢复(如果没有,就是backup导入没有成功)
> 如果这里没有 `从内部存储恢复` ，点击从 `外部存储`，然后把权限全部打开。
> 返回重新进入 `备份和恢复`，就会有了。

<font color="#00b050">如果成功，继续第4步。</font>
<font color="#ff0000">如果还是没有从”从内部存储恢复”，一定注意文件位置是否复制错误。(0步准备工作)</font>

## 4. 激活谷歌服务助手

`设置` - `系统和更新` - `日期和时间` - 将 `自动设置` 打开

从桌面打开 `谷歌服务助手` ，点击 `激活`,并给权限

> 🚨如果打开提示 `当前设备不支持` ，那就可以放弃治疗了
> 如果提示 `网络连接异常` ，说明也是可以支持的，只需要通过ADB降级**备份和恢复**的版本。[具体教程点击](https://toalan.com/archives/48/)

激活后**不**需要点击 `开始下载` ，直接返回桌面

## 5. 安装MicroG,且登录谷歌账号

> 软件在解压后的文件夹 `GMS安装软件`里，该步骤为 `第五步`，那么就看 `第五步` 的文件夹内容，其他同理。

><font color="#ff0000">⚠注意！如果你是企业谷歌账号，请不要添加，本教程不支持。</font>
><font color="#ffc000">注意：如果有多个账号，在这里一次性把账号添加完，后续不支持再添加账号，如需再添加账号或修改密码需要重新安装。</font>

安装 `microG` ,打开后点击 `Account` ，点击右下角 `sign in` ，登录自己的谷歌账号(此过程可能会闪退一两次, 重试即可)

## 6. 安装多个谷歌软件

1. 安装 `1` 、`2` 、`3` 、`4` 
2. 然后装 `5-3` ，如果 `5-3` 无法正常安装，就装 `5-2`（**这两个只装一个，优先装5-3**）

## 7. 卸载MicroG

1. `设置` - `应用和服务` - `应用管理` -搜索 `microG` 卸载

## 8. 安装Play服务

 1. 安装 `7.Play服务`，安装完之后,十秒左右状态栏便会报错("此设备未获得Play保护机制认证"),不用管.（<font color="#c00000">如果不弹窗，请检查网络是否正常，这个很重要！</font>）
 2. **不要**安装第八步的 `play商店` ，按照后续指示安装。

## 9. 下载Edge浏览器

1. 华为应用商店搜索 `Edge` ，下载并安装。
	  不要用 `华为浏览器` 、`夸克` 、`QQ浏览器`、`UC浏览器` 等其他毒瘤浏览器，会导致不跳转。

## 10. 通过ADB停用GSF【重要步骤！】

1. 准备一台PC电脑（win系统）和数据线。[button color="info" icon="command" url="https://toalan.com/archives/29/" type=""]MAC系统下这个[/button]
2. 下载`搞机工具箱V9.10`到电脑[button color="success" icon="download-cloud" url="https://www.123pan.com/s/x9tA-A8UW3.html" type="round"]（国内）123网盘下载[/button]/[button color="success" icon="download-cloud" url="https://1drv.ms/u/s!Atp0UM8FnZB_j5F7eGRR0eFMb5WJxA?e=5tKufr" type="round"]（国外）OneDrive网盘下载[/button]
3. 手机端操作：
	1. 手机通过数据线到电脑。
	2. 下滑通知栏，点击 `正在通过USB充电`,选择 `传输文件`模式。
	3. 打开 `开发者模式`（设置-关于手机-连点7次HarmonyOS版本-输入密码)
	4. 开启 `USB调试` （设置-系统和更新-开发者人员选项），弹窗都允许。
4. 电脑端操作:
	1. 解压压缩包，双击打开 `搞机工具箱v9.exe` 
	2. 如果一切正常，可以正常打开界面。（如果你连接有问题， 界面都不会弹出。怎么解决链接问题看弹窗提示帮助或者[点击这里跳转](https://www.bilibili.com/read/cv16541940/)或下载华为手机助手）!
5. 注意！下面的操作是很关键的，请仔细阅读。<font color="red">！！！重要！！！请阅读完剩余步骤，理解后再操作。</font>
	1. 点击左侧ADB终端，输入命令到上面**输入框**：`adb shell pm disable-user --user 0 com.google.android.gsf ` 注意！不要回车执行操作！只是粘贴上去好准备。
		![禁用](https://cos.toalan.com/alan_image/bf063af2590e49debcc593262989f993.png)
	2. 手机安装第八步的 `8.play商店` 。
		- 安装完打开后,会提示"我们正在为您更新Google Play",当跳出可以前往google商店的选项后，直接前往商店，跳过更新。
		- 如果商店可以正常打开加载数据，关闭play商店后台运行。<font color="red">注意，在教程没有结束之前，不要通过play下载任何应用。</font>
	3. 禁用GSF并且留住FCM功能操作。
		- 手机复制链接 `https://play.google.com/store/apps/details?id=com.google.android.gms` 到 `Edge` 打开。
		- 下方提示 `外部应用打开`，打开paly商店开应用详情页。
		- 点击更新，要注意下载的进度条，当进度条超过50%以后，立马用 `搞机工具箱` 禁用（命令框回车↩︎）。忽略提示信息，继续卸载
		- 命令窗口提示，表示成功，等待play服务更新安装完即可。![禁用GSF成功](https://cos.toalan.com/alan_image/a39552fb10d841799bf562bee16f53f2.png)
		- 更新完成后，play服务弹窗就会消失，消失后关掉play商店后台，重新打开，随便下载一个应用，正常下载继续11步。

> 如Play商店不能正常加载数据或报错，卸载 `Google 服务框架` 、`Google Play 服务`、`Google Play 商店`，重新安装 `Google 服务框架`（第六步，5-2/5-3） 。
> 从第八部开始重新操作。（可省略第九步）

## 11. 最后设置

为了确保谷歌服务正常的允许，建议进行以下设置。

1. `设置` - `应用和服务` - `应用管理` ，将 `Google Play 服务` 权限，开启所需权限。位置、媒体和文件（必开）
2. `设置` - `应用和服务` - `应用启动管理` ，将 `Google Play 服务`、 `Google Play 商店` - 设置为 `手动管理`，全选。

## 12.FCM使用方法

### 1. 检查FCM是否开启

1. 确保网络畅通可访问[谷歌](https://google.com)
1. 打开 `电话`，输入 `*#*#426#*#*` 跳转到FCM日志
2. 提示 `Connected` 表示已连接，即成功。
	```
	Server:Connected
	Host:mtalk.google.com/28.0.0.5
	Port:5228
	Time Connected:00:01
	```

> 如果Host和Port有数据，而Server提示No Connected，点一下EVENTS，再点一下STATUS，如果不行请重启手机。

### 2. FCM文字教程

`设置` - `应用和服务` - `应用启动管理` - 需要 FCM推送的软件 - 设置为手动管理，全选。

>比如：你想要Telegram收到消息推送，那么你就把Telegram设置为手动管理。

- 视频教程地址：[https://share.weiyun.com/xJalitfj](https://share.weiyun.com/xJalitfj)

---

🎉🎉🎉至此，教程内容已全部结束！
**研究技术**和**整理教程**不易，还希望老板们可以<font color="#00b050">真金白银</font>的支持一下（文章底部有打赏按钮）。
当然白嫖的话也是可以的，不过记得评论分享下**成功时间**和**设备型号+系统版本**。
如果你有**优化建议**的话，也可以提出来，您的互动，可以让后人享受到更好地教程体验。

感谢您的慷慨赞助！
![image](https://github.com/user-attachments/assets/0b3cae18-e190-4387-b4d6-3769d6a3b451)
![image](https://github.com/user-attachments/assets/e792323e-9f37-4789-ba0b-68b07c99b4eb)




# ✨常见问题汇总
---
## 1. 如何升级Play服务

>截止<u>2024年07月04日</u>写稿
>
>Google商店（Google Play Store）最新版本为：**41.6.29**
>GooglePlay服务（Google Play Services）最新版本为：**24.23.35**

>Google商店（Google Play Store）默认会自动更新，不需要手动更新
>GooglePlay服务（Google Play Services）可以在`应用和服务` - `应用管理` 找到该应用，最下面应用详细，点击跳转商店页面，更新即可。

## 2. 什么手机型号可以安装，荣耀系统可以么？

手机系统大部分都是可以安装的，平板现在也支持了（部分型号，看[microG安装使用GMS教程 - Alan's Blog - 个人博客 (toalan.com)](https://toalan.com/archives/71/)）
荣耀系统也可以。
具体型号看[华为荣耀支持GMS手机型号列表 - Alan's Blog - 个人博客 (toalan.com)](https://toalan.com/archives/46/)

## 3. Harmony-NEXT版本可以安装么？

我个人也是要一直使用的，以后NEXT版本出了，我会第一时间找到解决方法（欢迎大牛联系讨论-备注来意）。

注意，如果你需要使用GMS服务，请不要更新到Next系统，更多信息关注[叫我Alan的个人空间-叫我Alan个人主页-哔哩哔哩视频 (bilibili.com)](https://space.bilibili.com/95698600?spm_id_from=333.1007.0.0)或者我的[本站博客](https://toalan.com)。

## 4. 成功以后可以用应用分身、悬浮框、隐私空间么？

可以。
>开完分身后，一直弹窗说“play未获得保护机制认证”，注意看，弹窗右下角是有一个2的标志，说明是分身空间的play服务在作怪，其实不影响使用，当出来以后，右滑把他关闭就好了，如果你不永远不想看到他，看下面的步骤。

**最近有人发现开启分身后会立马弹窗**

>解决办法：清理所有后台应用-断网（流量和WIFI都要断掉）-启用分身。

---
 **终极解决应用分身弹窗问题**

>请将下面命令的xxx换为你分身用户的 `ID` 分别执行三次ADB命令
>	该ID是随机的，如何看分身ID命令为 `adb shell pm list users`
>	隐私空间同理，这两个功能本质都是多用户

```
adb shell pm disable-user --user xxx com.google.android.gsf
adb shell pm disable-user --user xxx com.google.android.gms
adb shell pm disable-user --user xxx com.android.vending
```

## 5.操作完成后之前的文件怎么处理？

- 谷歌服务助手（可删，但建议保留）
- 压缩包内容（可删）
- Device（可删）
- Play Services Info（可删）
- 设备信息（可删）

## 6.ChatGPT问题汇总

### 打开后转圈、打不开?

> 请检查是否能够正常访问 [ChatGPT](https://chatgpt.com)

### 打开后弹窗不能用?

提示该弹窗
```
Something went wrong
Check that Google Play is enabled on your device and that you're using an up-to-date version before opening the app.if the problem persists try reinstalling the app.
```
>请打开play商店再打开ChatGPT。
>
>**永久解决该问题方法：**
	1. 设置-应用和服务-应用启动管理-搜索 `Google Play 商店` 
	2. 将自动管理关闭，改为手动管理，全选确定。

###  Play商店 搜索不到 ChatGPT?

>复制链接`https://play.google.com/store/apps/details?id=com.openai.chatgpt` 到 `Edge` 打开，跳转到详情页。

### 提示 你所在的地区不支持?

查看自己的谷歌账号是否绑定了香港地区，香港被禁止使用ChatGPT

>**查看方法**：
>	打开play商店-点击头像-设置-常规-账号和设置偏好设置
>	
>	如果 `国家/地区和个人资料` 香港并且右侧打勾，说明你的账号已经绑定了香港地区，那么这个账号是无法使用chatgpt的（除非你绑定以前购买过chatgpt）
>
>**如何解决：**
	1. 更换地区（去网上搜教程或者找我远程）
	2. 或者多添加一个非绑定香港的谷歌账号。


## 7.极个别应用无法正常使用

因为有些软件需要更底层的谷歌服务，需要手机Root刷更底层服务，有方法，但我这里不做教程，大牛请绕道。

如果你发现你需要的应用用不了，欢迎评论反馈。

### **因服务受限应用（目前无法解决）：**
- Google Pay（谷歌钱包）
- Android Auto（安卓汽车APP，有方法用，我不作解释）（海外版EMUI系统可以使用）
- Gcam（谷歌相机）
- McDonald's (全球版)
- 更多发现中。。。

### **因谷歌位置服务受限应用（建议使用[Gbox](https://gboxlab.com/)）：**
- Getir
- Tokyo 迪士尼APP
- 谷歌Earth（可解决，位置权限选择 `允许本次使用`）
- Tinder
- strava
- 日本环球影城（usj）
- 更多发现中。。。

### **因网络受限应用（可解决）：**
- Tiktok（具体方法后续会更新教程）
- 领英（需要全局网络或国外SIM卡）
- NetFix
- Google Map 点评（需关闭 +86开头的手机卡）
- 更多发现中。。。

---
🔊如果帮助到你且条件允许的话，麻烦打赏一下，想凑个服务器钱。如需要一对一帮助可以[联系我](https://toalan.com/cross.html)（备注打赏信息）
