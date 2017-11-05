# kevinlq.github.com

## 声明

本博客框架是使用开源的jekyll.先后从以下几个博主clone过来主题进行写作.

- 2017.03 [daodaoliang](http://daodaoliang.com/)
- 2017.11 [mazhuang](http://mazhuang.org/)

在此非常感谢以上作者做出的贡献.

我也会在此基础上不断的进行修改.


## 效果预览

**[在线预览 &rarr;](http://kevinlq.com/)**

![screenshot home](http://mazhuang.org/assets/images/screenshots/home.png)

## 修改记录


![工程项目](/doc/project.png)

### 1. 添加网易云跟帖功能

修为多说评论系统为网易云跟帖(因为发现多说系统官网显示到2017年6月1号到期，然后停止维护，所以不得已选择其他的评论系统各。经过搜索发现网易云跟帖还不错就直接替换了，替换过程也很简单，虽然本人不是搞前端的，但是还是三下五除二给替换了)

替换后的效果如下所示：

![评论系统](/res/img/blog/project.png)


### 2. 添加百度统计功能
添加百度统计可以实时查到博客的访问量，百度了下操作起来也不难

* 申请账号
* 添加域名
* 获取代码
* 代码安装
* 安装检测

在实际操作过程中还是遇到了问题，找了半天还是没有找到，最后通过安装windows下jekyll编译工具才找到了问题，原来是标点符号的问题

```
tongji: f9a2a52ccc103ed91088462c5836c854 # 百度统计ID
```

**上述tongji冒号后面有个空格，若没有空格解析会出现问题的**

因为没有空格原因，导致github给我发个10多条错误提醒邮件，惭愧啊

## 3. 使用有言评论框架

之前使用的网易云跟帖，8月初通知说停止运营了，使能含泪放弃了，不知道是出于什么原因。

搜索了下发现有言还行，直接导入使用

ps:因为之前好多文章中使用wangyiyun这个昵称，修改工作量大，所以直接在wangyiyun.html中添加了有言插件代码

![评论系统](/res/img/youyan.png)