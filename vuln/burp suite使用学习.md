#### 模块介绍

```
1.Dashboard（仪表盘任务模块）
（1）Tasks：扫描漏洞任务
（2）Event log：事件日志
（3）issue activity：动态发现的问题
2.Target模块（目标请求响应全部记录）
（1）Site map：爬取出来的站点地图
（2）Scope：分别是在范围的显示和在范围内的不显示，支持正则表达式
（3）Issue definitions:一些漏洞信息 
（4）Filter:过滤规则设置
3.Proxy（代理模块 ）
（1）Intercept:拦截信息
（2）HTTP History:历史拦截信息
（3）WebSockets history：记录WebSockets数据包
（4）Options:代理监听，请求和响应，拦截反应，匹配和替换，ssl等规则设置
4.Intruder模块（入侵自动化攻击）
（1）Target:目标
（2）Positions:
Sniper:一个字典，两个参数，先匹配第一个参数，再匹配第二个参数
Battering ram:一个字典，两个参数，一个字典同时匹配两个参数，同用户名同密码
Pitchfork:两个字典，两个参数，两个字典分别匹配两个参数，到短的截至
Cluster bomb:两个字典，两个参数，交叉匹配(使用第一个字典的第一项匹配第一个
参数，然后遍历第二个字典)，所有可能 
（3）Payloads：载荷，字典选择，预置规则处理字典（如转换为md5值 ）
（4）Options：Intruder的各种设置
5.Repeater模块（请求重放）
Repeater的操作界面中，左边为请求消息区，右边为应答消息区，当编辑完请求消息后，单击"GO"按钮即可发送请求给服务器，应答消息区显示的是服务器端的反馈消息，通过修改请求消息的参数来比对分析每次应答消息之间的差异。
6.Sequencer(序列器)
（1）Live capture：信息截取
（2）Manual load：手动加载
（3）Analysis options：选项分析
6.Decoder模块（编码解码）
7.Comparer模块（对比）
8.Extender模块（插件扩展api）
9.User options模块（用户设置）
```

#### 证书导入

- [证书导入](https://zhuanlan.zhihu.com/p/547973012)
- 从bp的导出证书
  ![image-20230714002457258](http://150.158.87.220:9000/typora/blog/99862_168926549774377.png)
- 导入到钥匙串中， 并且设置权限
  ![image-20230714002621497](http://150.158.87.220:9000/typora/blog/99862_168926558175649.png)

----

#### 代理插件

- **proxy switchyOmega**
- [下载地址](https://link.zhihu.com/?target=https%3A//addons.mozilla.org/zh-CN/firefox/addon/switchyomega/)

---

#### proxy

- 