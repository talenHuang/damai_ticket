#### 提前准备
* Python 3.6+
* Chromedriver.exe
* Chrome 浏览器安装好后需将chromedriver.exe放置于Chrome浏览器目录下
* pip install selenium

#### 参数设置

在`config.json`中输入相应配置信息，具体说明如下：

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

![在这里插入图片描述](https://img-blog.csdnimg.cn/fcb3eec3cc3b41b5bc597c221ef71b6c.png#pic_center)

### 2021.12.10 更新
* 根据粉丝反馈，支持【日期】选择功能
![在这里插入图片描述](https://img-blog.csdnimg.cn/efa9d7b9825b46caa700bd72a9c9ee89.png)

### 2021.12.10
* [薛之谦演唱会](https://detail.damai.cn/item.htm?spm=a2oeg.search_category.0.0.57344206jb38CA&id=658630460380&clicktitle=%E8%96%9B%E4%B9%8B%E8%B0%A6%E2%80%9C%E5%A4%A9%E5%A4%96%E6%9D%A5%E7%89%A9%E2%80%9D%E5%B7%A1%E5%9B%9E%E6%BC%94%E5%94%B1%E4%BC%9A-%E5%B9%BF%E5%B7%9E%E7%AB%99)
* [李荣浩广州演唱会](https://detail.damai.cn/item.htm?spm=a2oeg.search_category.0.0.7e141ffaOOsGL3&id=660857675535&clicktitle=%E6%9D%8E%E8%8D%A3%E6%B5%A9%E2%80%9C%E9%BA%BB%E9%9B%80%E2%80%9D%E5%B7%A1%E5%9B%9E%E6%BC%94%E5%94%B1%E4%BC%9A%20%E5%B9%BF%E5%B7%9E%E7%AB%99)
* [北京保利·央华“神州九城，共享明天”2021演出行动 央华版 如梦之梦](https://detail.damai.cn/item.htm?spm=a2oeg.search_category.0.0.310919488fszNB&id=662432820667&clicktitle=%E4%BF%9D%E5%88%A9%C2%B7%E5%A4%AE%E5%8D%8E%E2%80%9C%E7%A5%9E%E5%B7%9E%E4%B9%9D%E5%9F%8E%EF%BC%8C%E5%85%B1%E4%BA%AB%E6%98%8E%E5%A4%A9%E2%80%9D2021%E6%BC%94%E5%87%BA%E8%A1%8C%E5%8A%A8%20%E5%A4%AE%E5%8D%8E%E7%89%88%E3%80%8A%E5%A6%82%E6%A2%A6%E4%B9%8B%E6%A2%A6%E3%80%8B)

