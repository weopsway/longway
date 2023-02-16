## WeOpsWay自动化管理平台-序篇

多种公有云以及本地虚拟机、k8s容器环境等，平时管理起来也不是很方便。想找一个免费的并且适合自己的多云管理平台又很难，这也是决定自己扣钉的初衷。

疫情的这两年，感觉时间过得很快，但愿留点看得见的东西，有所沉淀。

##### 开发架构
架构采用： Python+Django,AdminLTE+Layui,Mysql+Redis

基本功能： CMDB + Ansible/Shell管理 + 任务调度 + 应用发布 + 多云管理 + 多k8s集群管理 等

##### 多k8s集群管理
目前正在开发过程中，仅完成了一些基本的功能，刚完成了deploymnet的弹性收缩，版本回滚，在线通过yaml修改配置。
<iframe src="//player.bilibili.com/player.html?aid=651976223&bvid=BV1qe4y1F7YP&cid=1011031440&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

##### 多云管理
目前支持AWS，阿里云，Azure云主机的管理，并结合CMDB可以进行日常的各种运维工作.
<iframe src="//player.bilibili.com/player.html?aid=949386838&bvid=BV1vs4y1a7R3&cid=1011050165&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

##### Ansible管理
上面cmdb中主机的信息采集会调用ansible的接口，下面应用发布也会用到ansible的接口。
<iframe src="//player.bilibili.com/player.html?aid=224431246&bvid=BV1Eb411R7GV&cid=1011059521&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

##### 应用发布
类似于简单的jenkins，可以进行项目发布配置，然后选择应用不同的tag/bracher进行发布
<iframe src="//player.bilibili.com/player.html?aid=651965709&bvid=BV11e4y1F7WF&cid=1011027483&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

##### 监控平台
后面会有单独的监控管理平台，采用的无客户端安装模式进行数据采集， 包含硬件、基础架构，多云，容器云，OS，中间件，数据库等，并接入zabbix/promethue等各种监控api，集成Slack/钉钉/微信/邮件/短信/电话，实现AllInOne的告警平台以及故障自愈
目前还在开发中，仅完成OS层面的监控和告警,下一版本将加入减少告警噪音的功能.

##### 自动化和智能化的探讨
关于IT自动化和智能化，这个话题一直都在讨论，个人觉得自动化更注重于将多云(包含容器云)，devops, os/mw/database日常运维, 多任务批量调度，工单系统，多维可视化，多平台全链路安全监控日志告警等融合集成一体化，目标应该就是AllInOne的一体化运维平台，全链路监控，流程审批，安全审计以及开发、运维、项目管理等。既能适用于运维人员，也适用于开发和项目管理人员等。

IT智能化应该更偏向于单个具体产品的使用，比如数据库智能平台，能够将数据库运维的经验以及数据库监控指标相结合，通过多维度多场景实时监控数据库，发现异常能及时告警，常见的问题能够做到故障自愈，复杂的问题能给出具体判断点做到精准点位，而我们作为使用者只需要看看告警内容然后按下流程确定键，下一步后台就可以进行自动修复了。目标很明确，实现起来却是很难，需要有相关产品运维经验丰富的专家团队，运维开发团队以及大数据量、各种应用场景支撑测试验证等等。

待续

