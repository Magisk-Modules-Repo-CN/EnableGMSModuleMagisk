GMS = Google Play Services  
  
## 简要说明

我发现GMS在后台时的活动过于激进。众所周知，过于活跃的GMS正是导致设备疯狂耗电的罪魁祸首。

## 想法 以及 实际情况

Google从Android 6.0开始，推出了 Doze ( [点击这里快速了解Doze](https://www.howtogeek.com/242563/how-androids-doze-improves-your-battery-life-and-how-to-tweak-it/))它有助于让应用进入潜度休眠状态，也就是我们常说的「打盹」。  
  
应用进入「打盹」状态后，能在保持功能正常使用的情况下降低耗电量。  
  
但问题是，GMS无法进去「打盹」。因此，它无法减少GMS的耗电量。当然Google这么设定也是有原因的（请阅读下方 注意事项 部分以进一步了解）

## 解决方案

快速了解（如果您有兴趣请点[这里](https://android.stackexchange.com/questions/143247/how-to-make-google-play-services-and-other-default-white-listed-system-apps-doze))  
  
原理很简单，默认情况下你是无法在Doze列表看到GMS的。这个模块的作用就是将GMS从Doze的白名单显示出来。

接着，我们只需要将GMS从Doze白名单中移除，这样GMS就能够进入「打盹」状态。

这就是这个模块所做的所有事情，并且是Systemlessly。

通过本模块，您可以将GMS从“Doze白名单”列表移至“优化列表”中，使得GMS可以进入「打盹」状态以节省一部分耗电。

安装了Android7或更高版本的系统的 一加手机用户 无法找到此选项。但还是可以从设置中的“GMS”应用信息中，选择电池选项以检查优化状态。

## 注意事项
  
省电不会导致出现问题，这种方法也是如此。  
  
通过在GMS开始「打盹」，正常情况下会导致GMS延迟或暂停某些服务。其中有一个我们能感知到的，就是GCM通知服务的延迟。  
  
当设备已经处于「打盹」状态时，使用相关服务的部分应用程序会有一定的通知延迟。  
  
但，根据我个人的情况来看(我在我的三个设备上都用了这个模块），我的LINE，WhatsApp和Telegram的通知一切正常。 （在我把这些应用放入白名单的前提下）  
  
我注意到的那个稍有延迟的是Gmail。但是我个人习惯自行开邮箱查阅邮件，所以这个对我来说影响不大。  
  
至于其他方面，例如 账户同步，铃声，位置服务以及其他的什么东西，都没有任何问题。  
  
GPS工作正常，通知响铃正常，帐户同步正常。  
  
## 更新日志
### v1. 
    - 初发布
### v2. 
    - Magisk模板更新
### v3. 
    - 代码精简
### v4. 
    - Magisk模板更新至13.3
### v5. 
    - Magisk模板更新至13.3 - 请更新你的 Magisk Manager
### v6. 
    - Magisk模板更新至15 - 兼容Oreo

## 支持
你可以在 @XDA找到我的这个项目 : [点击这里跳转](https://forum.xda-developers.com/apps/magisk/module-enable-doze-google-play-services-t3608783/post72344542#post72344542)

## 版权所有
otonieru@xda-developers - 2018
如果您希望该模块适配您使用的ROM，请告知于我 : )
