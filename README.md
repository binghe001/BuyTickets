# 作者及联系方式
作者：冰河  
QQ：2711098650  
微信公众号： 冰河技术

# 项目
实现自动抢火车票(基于Python3.6+splinter)

# splinter使用
plinter.brower是一个开源工具，通过Python自动化测试ｗｅｂ，通过电脑自动操作网页。
Splinter模块是python egg，下载当然很简单，安装： pip install splinter
同时还需要浏览器的驱动，Splinter的Browser类默认优先调用的驱动是firefox，所以用chrome的话需要在初始化Browser时候指定driver_name="chrome"参数，建议都明确指定浏览器！
注意：Chrome的驱动chromedriver，注意版本要对应，不然基本上会有unknown error，打不开浏览器
splinter.brower基础知识：
创建一个Browser实例，就会打开相应的浏览器。
visit(url): 故名思议，访问指定网站
findbyid("控件的id").first: 根据控件的属性id找到控件，一般控件都有独立唯一的id。不然，Splinter api还提供byname,byid,by_tag等方法！first表示返回第一次找到的控件。
fill("要填充的内容"): 用指定的内容填充相应控件
控件是指对数据和方法的封装。控件可以有自己的属性和方法，其中属性是控件数据的简单访问者，方法则是控件的一些简单而可见的功能、控件创建过程包括设计、开发、调试（就是所谓的3Ds开发流程,即Design、Develop、Debug）工作， 然后是控件的使用。
设计控件是一项繁重的工作。自行开发控件与使用控件进行可视化程序开发存在着极大的不同，要求程序员精通面向对象程序设计。创建控件的最大意义在于封装重复的工作，其次是可以扩充现有控件的功能。
click(): 点击控件
登录后，browser.cookies.all()中保存了本次登录的cookie信息（dict类型），可以打印出来或者保存下次使用
quit_browser(browser)函数: 要求用户交互输入q再退出。否则，程序跑完之后就直接退出了，释放Browser的实例，调用quit()方法，浏览器也就关闭了。
reload() 方法用于重新加载当前文档

# 实现思路：
首先我们需要登陆１２３０６网站，登录时需要输入用户名与密码，然后需要输入蛋疼的验证码，然后选择起、始站，时间，车次类型，点击查询，再选择车次，乘客，提交订单。如果按照这样的手动操作下来，票早已经没有了

# 实现目标：
整个流程全自动，自动登陆，自动查询，自动订单，自动提交订单（ (暂时不实现自动点击验证码，验证码成功几率比较低）

# 扫一扫关注微信公众号

**你在刷抖音，玩游戏的时候，别人都在这里学习，成长，提升，人与人最大的差距其实就是思维。你可能不信，优秀的人，总是在一起。** 
  
扫一扫关注冰河技术微信公众号  
![微信公众号](https://github.com/sunshinelyz/binghe_resources/blob/master/images/subscribe/qrcode_for_gh_0d4482676600_344.jpg)  
