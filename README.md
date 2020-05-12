# mini-program

```
miniprogram：
|- api                                 获取模块API数据
|- components                          自定义组件
|- iconfont                            iconfont图标集合
|- images                              图片集合（包含云开发DEMO图片）
|- pages                               页面展示集合
  |- home                              主页
    |- first                           主页 "Part one" 组件
  |- index                             下列均云开发Demo页面
|- style   
|- utils                               工具类
|- README.md                         
|- project.config.json               
```



## 云开发

1. 云函数 （需要上传并部署login / openapi）

>  1.1 云服务引用（参考：[全局常量](https://www.jianshu.com/p/e3de2c605506)）

>  1.2 async await与API模块化引用 *小程序是不支持 async-await 语法的，可以使用 Facebook 开源库 regenerator

2. 数据库

3. 环境（支持创建两个环境，所以：project-dev, project-pro）

4. 非关系型数据库



## 全局守卫

  1. api请求时判断是否含有token，没有则重定向到login
  
  2. 第三方库（全局判断是否登录）：https://www.jianshu.com/p/8f33a38a671a



## 全局变量
```
const app = getApp() //全局app.js
app.globalData.userInfo //引用方式
```



## 自定义组件的引用

### 全局声明引用（app.json）、局部声明引用（当前文件夹中**.json）

### 父子组件传值/事件

- 父组操作子组件方法：使用`this.selectComponent()`操作子组件方法

- 父组传递值至子组件：`<parent prop="{{hello}}" />` 与 `properties: {prop: null}` 、 `this.properties.prop` 

- 子组件触发父组件方法： `this.triggerEvent()`, 类似Vue方式

### 局部组件声明引用（头部、尾部等） 或者动态加载组件

```
  <import src='./head.wxml' />
  <template is="head" data="{{data}}"></template>
```



## WXML中使用函数方式： 

*.wxml
```
  <view>{{ parse.color() }}</view>
  <wxs module="parse">
    module.exports = {
      color: function () {
        // do something
        return **
      }
    }
  </wxs>
```



## 需要在WXML引用库的方式：Date中使用函数赋值： `Date: {isNumber: util.isNumber()}`



## `wx.getStorageSync('key')` 用于保存token、角色等信息



## 引用第三方UI库iview、vant等



## input获取焦点时布局上移



## 小程序使用iconfont

[参考文章](https://www.jianshu.com/p/0d631d3b1983)

1. https://www.iconfont.cn/home/index 下载

2. https://transfonter.org/ 转换ttf格式

3. 转换下载得到stylesheet.css

4. iconfont icon-xx



## rpx vw/vh 单位

`1rpx = (viewport / 750)px  //（viewport代表当前设备宽度）`

`1vw/vh // 代表当前设备的宽度/高度百分之一`



## 云开发-上传

直接使用云开发提供Demo即可实现（PC端会失败， 真机调试成功）

* 图片存放在 云开发->存储中



## 图片优化

[https://imagecompressor.com/zh/](https://imagecompressor.com/zh/)



## 多图上传优化

- 异步加载

- canvas优化质量（最小清晰度）



## 微信支付

微信支付 + 云开发参考： 

[https://developers.weixin.qq.com/community/develop/doc/000620ec5acb482103b7bf41d51804](https://developers.weixin.qq.com/community/develop/doc/000620ec5acb482103b7bf41d51804)

[https://ruby-china.org/topics/38786](https://ruby-china.org/topics/38786) 

Node后端:[https://blog.csdn.net/qq_36607860/article/details/86159825](https://blog.csdn.net/qq_36607860/article/details/86159825)

