# APNS


## 1.APNSProduction 设置的坑    

很多时候，当应用发布时，突然发现推送功能失效了，查了很久的资料也没差出个所以然，在调试阶段貌似好好的（这里的情况包括，比如先发了一个ad_hoc 测试包，发现无法推送，再用Xcode 往手机装了一下，推送OK）。    

但当传到App  Store 之后发现  都推不了了，在确保各种证书都没有问题的情况下，很有可能是后台忘了配置APNsProduction 的值，该值默认为false，当发布至App Store 之后该值应设置为true 这样App Store 上的版本就可以正常收到通知消息了。    