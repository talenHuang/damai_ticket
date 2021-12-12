#### 提前准备
* Python 3.6+
* Chromedriver.exe
* Chrome 浏览器安装好后需将chromedriver.exe放置于Chrome浏览器目录下
* pip install selenium

#### 参数设置

在`config.json`中输入相应配置信息，具体说明如下：

* `date`: 日期选择
* `sess`: 场次优先级列表，如本例中共有三个场次，根据下表，则优先选择1，再选择2，最后选择3；也可以仅设置1个。
* `price`: 票价优先级，如本例中共有三档票价，根据下表，则优先选择1，再选择3；也可以仅设置1个。
* `real_name`: [1,2], 实名者序号，如本例中根据序号共选择两位实名者，根据序号，也可仅选择一位
  * 选择一位或是多位根据购票需知要求，
  * 若无需实名制信息则不需要填写，
  * 若一个订单仅需提供一位购票人信息则选择一位，
 * 若一张门票对应一位购票人信息则选择多位）。
 
* `nick_name`: 用户在大麦网的昵称，用于验证登录是否成功
* `ticket_num`: 购买票数
* `damai_url`: https://www.damai.cn, 大麦网官网网址
* `target_url`: https://detail.damai.cn/item.htm?id=599834886497  目标购票网址

* 部分门票需要选择城市，只需选择相应城市后将其网址复制到config.json文件的target_url参数即可。

* 根据需要选择的场次和票价分别修改config.json文件中的sess和price参数。

* 查看购票须知中实名制一栏，若无需实名制则config.json文件中的real_name参数不需要填写（即为[]）；若每笔订单只需一个证件号则real_name参数只需选择一个；若每张门票需要一个证件号，则real_name参数根据需购票数量进行相应添加。


* 若是首次登录，根据终端输出的提示，依次点击登录、扫码登录，代码将自动保存cookie文件（cookie.pkl）

* 使用前请将待抢票者的姓名、手机、地址设为默认。

* 配置完成后执行python damai_ticket.py即可,注意观察控制台输出。

* 本代码为保证抢票顺利，设置循环直到抢票成功才退出循环，若中途需要退出程序请直接终止程序。

### 2021.12.1 更新
* 脱离python和chrome浏览器环境，生成exe执行文件
* 下载地址：https://blog.csdn.net/weixin_35770067/category_10696190.html

订阅CSDN文章后有问题，可以添加我的联系方式：
<p align="center">
<img width="200" src="https://user-images.githubusercontent.com/37463338/145716647-5bf61260-c1d5-4a4a-9b85-ce8dedf8aeeb.png">
</p>


### 2021.12.12 更新
感谢[Fly1nDutchman](https://github.com/ouyangjunfei?tab=repositories)在其他购票页面发现的问题，经过验证，我已经合并代码，特再次进行说明，表示感谢。

修复1：支持关闭实名制遮罩
* 测试地址：https://detail.damai.cn/item.htm?&id=662062693636
<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/37463338/145715661-56e0a495-2809-461e-beb2-7030fbe8e748.png">
</p>

修复2：特惠场次有票但无法被选中的问题
* 测试地址： https://detail.damai.cn/item.htm?id=659519464426

修复3：支持日期选择
<p align="center">
<img width="500" src="https://user-images.githubusercontent.com/37463338/145716541-e74a3624-7ebf-45c0-ae64-c30e2211af9e.png">
</p>

### 后续更新计划
* 计划增加座位选择，有些演唱会可以在线选座，等于到的时候我再加上去吧。
* 优化代码抢购时间
* 写一个漂亮的c#界面
* 本周五在现抢购南京德云社的门票，喜欢的女生是德云社铁粉，平时最喜欢看《乡村爱情1-13》《刘老根》等一系列节目，有一起抢的小伙伴可以约起来。

### 赞赏
<p align="left"><strong>如果我的开源项目对你有所帮助，可以使用微信/支付宝请我喝杯咖啡</strong></p>

<p align="center">
<img width="300" src="https://user-images.githubusercontent.com/37463338/145717146-96da777d-3031-4f9a-9196-6345a95d2c2c.JPG">
</p>
<p align="center">
<img width="300" src="https://user-images.githubusercontent.com/37463338/145717159-fe59ed1d-f396-44c7-b2ac-3aa0bcafe074.JPG">
</p>

<center class="half">
<img src="https://user-images.githubusercontent.com/37463338/145717146-96da777d-3031-4f9a-9196-6345a95d2c2c.JPG" width="200"/><img src="https://user-images.githubusercontent.com/37463338/145717159-fe59ed1d-f396-44c7-b2ac-3aa0bcafe074.JPG" width="200"/>
</center>

<p float="left">
  <img src="https://user-images.githubusercontent.com/37463338/145717146-96da777d-3031-4f9a-9196-6345a95d2c2c.JPG" width="300" />
  <img src="https://user-images.githubusercontent.com/37463338/145717159-fe59ed1d-f396-44c7-b2ac-3aa0bcafe074.JPG" width="300" /> 
</p>


### 热门演唱会信息
* [薛之谦演唱会](https://detail.damai.cn/item.htm?spm=a2oeg.search_category.0.0.57344206jb38CA&id=658630460380&clicktitle=%E8%96%9B%E4%B9%8B%E8%B0%A6%E2%80%9C%E5%A4%A9%E5%A4%96%E6%9D%A5%E7%89%A9%E2%80%9D%E5%B7%A1%E5%9B%9E%E6%BC%94%E5%94%B1%E4%BC%9A-%E5%B9%BF%E5%B7%9E%E7%AB%99)
* [李荣浩广州演唱会](https://detail.damai.cn/item.htm?spm=a2oeg.search_category.0.0.7e141ffaOOsGL3&id=660857675535&clicktitle=%E6%9D%8E%E8%8D%A3%E6%B5%A9%E2%80%9C%E9%BA%BB%E9%9B%80%E2%80%9D%E5%B7%A1%E5%9B%9E%E6%BC%94%E5%94%B1%E4%BC%9A%20%E5%B9%BF%E5%B7%9E%E7%AB%99)
* [北京保利·央华“神州九城，共享明天”2021演出行动 央华版 如梦之梦](https://detail.damai.cn/item.htm?spm=a2oeg.search_category.0.0.310919488fszNB&id=662432820667&clicktitle=%E4%BF%9D%E5%88%A9%C2%B7%E5%A4%AE%E5%8D%8E%E2%80%9C%E7%A5%9E%E5%B7%9E%E4%B9%9D%E5%9F%8E%EF%BC%8C%E5%85%B1%E4%BA%AB%E6%98%8E%E5%A4%A9%E2%80%9D2021%E6%BC%94%E5%87%BA%E8%A1%8C%E5%8A%A8%20%E5%A4%AE%E5%8D%8E%E7%89%88%E3%80%8A%E5%A6%82%E6%A2%A6%E4%B9%8B%E6%A2%A6%E3%80%8B)
   * 黄牛加价2000+

