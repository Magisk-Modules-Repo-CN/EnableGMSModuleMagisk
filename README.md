GMS = Google Play Services  
  
## 简要说明

我发现GMS在后台时的活动过于激进。众所周知，过于活跃的GMS正是导致设备疯狂耗电的罪魁祸首。

## 想法 以及 实际情况

Google从Android 6.0开始，推出了 Doze ( [点击这里快速了解Doze](https://www.howtogeek.com/242563/how-androids-doze-improves-your-battery-life-and-how-to-tweak-it/))它有助于让应用进入潜度休眠状态，也就是我们常说的「打盹」。  
  
应用进入「打盹」状态后，能在保持功能正常使用的情况下降低耗电量。  
  
但问题是，GMS无法进去「打盹」。因此，它无法减少GMS的耗电量。当然Google这么设定也是有原因的（请阅读 SIDE EFFECT / NOTE 部分以进一步了解）

## 解决方案

快速了解（如果您有兴趣请点[这里](https://android.stackexchange.com/questions/143247/how-to-make-google-play-services-and-other-default-white-listed-system-apps-doze))  
  
原理很简单，默认情况下你是无法在Doze列表看到GMS的。这个模块的作用就是将GMS从Doze的白名单显示出来。

接着，我们只需要将GMS从Doze白名单中移除，这样GMS就能够进入「打盹」状态。

这就是这个模块所做的所有事情，并且是Systemlessly。

通过本模块，您可以将GMS从“Doze白名单”列表移至“优化列表”中，使得GMS可以进入「打盹」状态以节省一部分耗电。

安装了Android7或更高版本的系统的 一加手机用户 无法找到此选项。但还是可以从设置中的“GMS”应用信息中，选择电池选项以检查优化状态。

## The Side Effect/ Note
Saving energy never come without side effect. Same goes with this method.

By enabling Doze on Google Play Services, it will theoritically delay/pause some it's services. Most noticeable might be the GCM (cloud messaging) services.

App that use this services might experience delay in notification when Doze already kick in.

Although, in my experience (i use this mod on all of my three devices) my notif for LINE, WhatsApp and Telegram (my main comm app) is never been delayed. ( I put all these apps in my whitelist btw)

The one i noticed had slight delay is GMail. But i check my mail regularly throughout the day, so i need no real time notif for that.

As for all other main services like Accounts, Alarm, Location and elses, i never have any issue with them when i got this module active. GPS work fine, Alarm ringing, Account Syncing normally.

## CHANGELOG
### v1. 
    -Initial Release
### v2. 
    -Template Update
### v3. 
    -Code Cleaning
### v4. 
    -Template Update for Magisk 13.3
### v5. 
    -Template Update for Magisk 14 - PLEASE UPDATE YOUR MAGISK INSTALLATION
### v6. 
    -Template Update for Magisk 15 & Adding OREO Support

## Support
Find support on my thread @XDA : [Here](https://forum.xda-developers.com/apps/magisk/module-enable-doze-google-play-services-t3608783/post72344542#post72344542)

## Copyright
otonieru@xda-developers - 2018
If you wish to implement the modification into your ROM, please mention me :)
