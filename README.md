# XLChannelControl

### 说明

参考了今日头条、网易、腾讯这几个新闻客户端的频道管理功能，觉得腾讯的逻辑和操作还是比较清晰的，所以仿照这腾讯新闻的客户端做了一个这个频道管理的功能；
<br>
实现原理是利用UICollectionView+UIGestureRecognizer实现的。

### 功能

- [x] 拖拽排序已订阅频道
- [x] 点击删除、添加订阅频道
- [x] 固定第一个订阅频道，不可点击、拖拽

### 显示效果

| 正常显示 | 点击删除/增加 | 拖拽排序 |
| ---- | ---- | ---- |
|![image](https://github.com/mengxianliang/XLChannelControl/blob/master/GIF/1.gif)| ![image](https://github.com/mengxianliang/XLChannelControl/blob/master/GIF/2.gif)| ![image](https://github.com/mengxianliang/XLChannelControl/blob/master/GIF/3.gif)|

### 使用方法

```objc
[[XLChannelControl shareControl] showChannelViewWithInUseTitles:titleArr1 unUseTitles:titleArr2 finish:^(NSArray *inUseTitles, NSArray *unUseTitles) {
    //处理后续问题
}];
```
### 参数说明：
传入参数：
<br>
**titleArr1** ：已选频道集合 **titleArr2**：未选频道集合
<br>
返回数据：
<br>
**inUseTitles**：排序、增删处理后的已选频道 **unUseTitles**：增删后的未选频道

### 实现原理请参考[我的博文](http://blog.csdn.net/u013282507/article/details/54374952)

### 我之前用ScrollView实现的版本[戳这里](http://code.cocoachina.com/view/133979)

### 个人开发过的UI工具集合 [XLUIKit](https://github.com/mengxianliang/XLUIKit)
