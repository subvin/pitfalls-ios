# 极光推送


## 1.badge 字段的坑    

推送数目的坑，App Icon 右上角数目由后台推送的 badge 字段的数值就是推送的数目，一般来讲如果不需要显示该数值的时候，只需要后台配置该值设置为 0 即可，很多的应用都是让该值自动增长。极光推送该值得默认值目前貌似为 2，所有不管后台推了多少条通知 App 端看到的数值一直都是 2。    

解决方案：设置该值为  ‘+1’ 它就会自增长，其余的交由 APP 端来做，这也是后台很容易遗漏之处之一。    