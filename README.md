GMS = Google Play Services  
  
## 简要说明

我发现GMS在后台时的活动过于激进。众所周知，过于活跃的GMS正是导致设备疯狂耗电的罪魁祸首。

## 想法 以及 实际情况

Google从Android 6.0开始，推出了 Doze ( [点击这里快速了解Doze](https://www.howtogeek.com/242563/how-androids-doze-improves-your-battery-life-and-how-to-tweak-it/))它有助于让应用进入潜度休眠状态，也就是我们常说的「打盹」。  
  
应用进入「打盹」状态后，能在保持功能正常使用的情况下降低耗电量。  
  
但问题是，GMS无法进去「打盹」。因此，它无法减少GMS的耗电量。当然Google这么设定也是有原因的（请阅读 SIDE EFFECT / NOTE 部分以进一步了解）

## THE SOLUTION
Quick study (detail, if you are interested [Here](https://android.stackexchange.com/questions/143247/how-to-make-google-play-services-and-other-default-white-listed-system-apps-doze))reveal that Google put simple configuration is /system/etc/sysconfig/google.xml that WHITELISTING Google Play Services from the DOZE Mechanism.

So to make DOZE able to work on it, we simply need to remove the whitelisting.

This is WHAT THIS MODULE DO - SYSTEMLESSLY (obviously)

By installing this module, you can move Google Play Services from the "App Not Optimised" list to "App Optimised" which mean DOZE mechanism will work its magic on Google Play Services, thus should saving you more juices/batt throughout the day.

OOS (OnePlus) user with Nougat version and above installed wont find this option anymore. Instead, they should go to "Google Play Services" App Info from setting, choose the battery option, and scroll down to "Battery Optimisation" to check the status

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
