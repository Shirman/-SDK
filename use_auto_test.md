# 小程序自动化测试

## 小程序自动化测试技术方案
- Appium
    - [官网 http://appium.io](http://appium.io)
    - 支持 ios，android
    - 脚本语言python
- Airtest
    - [官网 http://airtest.netease.com/](http://airtest.netease.com/)
    - 支持 ios，android
    - 脚本语言python
    - 支持脚本录制
- Minium
    - [微信官方https://git.weixin.qq.com/minitest/minium-doc](https://git.weixin.qq.com/minitest/minium-doc)
    - 支持 ios，android，模拟器
    - 脚本支持python，javaScript
    - 内测中
- 小程序自动化SDK
    - [微信官方https://developers.weixin.qq.com/miniprogram/dev/devtools/auto/quick-start.html](https://developers.weixin.qq.com/miniprogram/dev/devtools/auto/quick-start.html)
    - 基于微信开发者工具，支持ios，andriod，源码调试
    - 脚本语言javaScript，需要Jest测试框架配合
- 更多方案...

## 选型过程
   - Appium 已经有技术团队落地并开源了技术方案：
   [有车以后 https://github.com/richshaw2015/wxapp-appium](https://github.com/richshaw2015/wxapp-appium)
   
   - Airtest 网易开源的移动端测试框架，基于图像识别，支持脚本录制，真香警告
   
   - Minium 微信官方团队的小程序测试框架，目前正在如火如荼的内测中，功能强大，号称别人有的它都有，别人没有的它有，亲儿子果然不一样
   
   - 小程序自动化SDK，是为开发者提供了一套通过外部脚本操控小程序的方案，从而实现小程序自动化测试的目
   
 ## 小程序自动化SDK之旅
 
 ### 我用它做了什么
   - 模拟用户浏览页面，检查数据展示是否正常
   - 根据用户的身份类型，检查数据展示是否正常
   - 浏览，页面跳转，下单
   - 模拟用户点击，滑动，长按操作
   
 ### 我用它做不了什么
   - 无法操作原生的组件，如弹出的提醒框，这导致我无法全流程自动下单
   - 不支持webview，无法测试webview相关页面
 
 ### 痛点
   - 不可不写的await，你几乎需要在每个获取元素的地方写上await
   - 不支持的链式书写方式。无尽的await，你可能会想用类似await $('.parent').$('.child')的语法，对不起不支持
 
## 总结
      小程序自动化SDK 对比 Minium，小程序SDK只不过是小程序自动化测试历史中官方缺少自动化测试框架的一个补充。但是他们应该又是殊途同归的，
    那便是基于微信开发者工具底层不变的命令行调用。相信随着Minium越发成熟，它的太子优势会越来越明显，那些小程序开放的API是其他自动化测试
    框架不曾能给到的体会。那么我们现在还有什么理由使用自动化SDK呢，它毕竟已经可以满足你大部分的测试需求了，不是吗？
      下期，我将隆重介绍微信官方框架Minium。
 
 
 
   

   
   
    
    

    
    