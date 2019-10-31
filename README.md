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
  |- addFunction                       
  |- chooseLib
  |- databaseGuide
  |- deployFunctions
  |- openapi
  |- storageConsole
  |- userConsole
|- style   
|- utils                               工具类
  |- app.js                            全局JavaScript
  |- app.json                          全局路由/导航栏/框配置
  |- app.wxss                          全局样式（组件内无法继承）
  |- sitemap.json
|- README.md                         
|- project.config.json               
```

## 云开发

1. 云函数 （需要上传并部署login / openapi）

>  1.1 云服务引用（参考：[全局常量](https://www.jianshu.com/p/e3de2c605506)）

>  1.2 async await与API模块化引用（最优解决方式，参考api文件）

2. 数据库

3. 环境（支持创建两个环境，所以：project-dev, project-pro）

4. 非关系型数据库
   

## 小程序使用iconfont

[实现方式](https://www.jianshu.com/p/0d631d3b1983)

1. https://www.iconfont.cn/home/index 下载

2. https://transfonter.org/ 转换ttf格式

3. 转换下载得到stylesheet.css

4. iconfont icon-xx

## 自定义组件的引用

### 父子组件传值/事件

```
父组传递值至子组件： properties

父组操作子组件方法：使用this.selectComponent()操作子组件方法
子组件触发父组件方法： this.triggerEvent()
```

## rpx vw/vh 单位

`1rpx = (viewport / 750)px  //（viewport代表当前设备宽度）`

`1vw/vh // 代表当前设备的宽度/高度百分之一`

## 云开发-上传

直接使用云开发提供Demo即可实现（PC端会失败， 真机调试成功）

* 图片存放在 云开发->存储中

## 图片优化

[https://imagecompressor.com/zh/](https://imagecompressor.com/zh/)

## 微信支付

微信支付 + 云开发参考： 

[https://ruby-china.org/topics/38786](https://ruby-china.org/topics/38786) 

[https://developers.weixin.qq.com/community/develop/doc/000620ec5acb482103b7bf41d51804](https://developers.weixin.qq.com/community/develop/doc/000620ec5acb482103b7bf41d51804)

Node后端:[https://blog.csdn.net/qq_36607860/article/details/86159825](https://blog.csdn.net/qq_36607860/article/details/86159825)

