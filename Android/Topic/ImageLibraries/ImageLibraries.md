# 图片库选型

## Picaso

### 优点

* 在Adapter中自动取消已经不在视野的加载。
* 支持优先级。
* 根据网络情况调整并发数量。

### 缺点

* 本身没有实现本地缓存，使用的是OKhttp的http请求缓存。
* 图片使用的色彩模式是ARGB_8888，占用更大的内存。
* 图片使用的原始大小。
* 加载速度更慢。
* 不支持gif。



## Glide

### 优点

* 支持GIF，Webp，Video。
* 支持Okhttp，Volley。
* 根据生命周期自动管理。
* 占用内存更少，使用RGB_565，根据into()的view大小缩放图片，而不是加载原始大小。
* 更高效的缓存。
* 使用Bitmap对象池。

### 缺点

* 包更大，500K > 100K。
* 方法数更多。
* 不支持渐进式加载。



## Fresco

### 优点

* 5.0以下，图片保存在匿名共享内存（Native堆），减少了OOM的可能。
* 渐进式加载。

### 缺点

* 包更大，2M。
* 使用复杂。
* 侵入性强。