## WeOpsWay自动化管理平台-序篇

多种公有云以及本地虚拟机、k8s容器环境等，平时管理起来也不是很方便。想找一个免费的并且适合自己的多云管理平台又很难，这也是决定自己扣钉的初衷。

疫情的这两年，感觉时间过得很快，但愿留点看得见的东西，有所沉淀。

##### 开发架构
架构采用： Python+Django,AdminLTE+Layui,Mysql+Redis

基本功能： CMDB + Ansible/Shell管理 + 任务调度 + 应用发布 + 多云管理 + 多k8s集群管理 等

##### 多k8s集群管理
目前正在开发过程中，仅完成了一些基本的功能，刚完成了deploymnet的弹性收缩，版本回滚，在线通过yaml修改配置。
<video id="video"  width="400" height="300" controls=""  preload="none" poster="https://img-blog.csdnimg.cn/a6e4664bcddc4076be1676cf9253e57e.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAd2VvcHN3YXk=,size_20,color_FFFFFF,t_70,g_se,x_16">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bc3viaawaaadeaean2s7frfbkwdbovaacya.f10002.mp4?dis_k=5e251290d12a8148f549fd969b2db821&dis_t=1652321254&spec_id=undefined1652321249&vid=wxv_2348277204310245377&format_id=10002&support_redirect=1&mmversion=false" type="video/mp4">
</video>

##### 多云管理
目前支持AWS，阿里云，Azure云主机的管理，并结合CMDB可以进行日常的各种运维工作.
<video id="video"  width="400" height="300" controls=""  preload="none" poster="https://img-blog.csdnimg.cn/035d4d09d18c4d67940f1f028cc9ba67.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAd2VvcHN3YXk=,size_20,color_FFFFFF,t_70,g_se,x_16">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bc3r4aawaaabyaez4cs7nrfbd6dbohqacya.f10002.mp4?dis_k=c3f457af4736e680c34d565c7b18be7a&dis_t=1652321310&spec_id=undefined1652321305&vid=wxv_2348259189875228673&format_id=10002&support_redirect=1&mmversion=false" type="video/mp4">
</video>

##### Ansible管理
上面cmdb中主机的信息采集会调用ansible的接口，下面应用发布也会用到ansible的接口。
<video id="video"  width="400" height="300" controls=""  preload="none" poster="https://img-blog.csdnimg.cn/bc7133ffd69e476fbd4174de99cd5fdb.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAd2VvcHN3YXk=,size_20,color_FFFFFF,t_70,g_se,x_16">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bc3buaayaaacmagriks3nrfadodbqgqadaa.f10002.mp4?dis_k=ae0a27eebba9ade7fac19ed4316004b1&dis_t=1652321348&spec_id=undefined1652321343&vid=wxv_2348382078318362624&format_id=10002&support_redirect=1&mmversion=false" type="video/mp4">
</video>

##### 应用发布
类似于简单的jenkins，可以进行项目发布配置，然后选择应用不同的tag/bracher进行发布
<video id="video"  width="400" height="300" controls=""  preload="none" poster="https://img-blog.csdnimg.cn/2b3b589b931448059b100fcb5632b656.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAd2VvcHN3YXk=,size_20,color_FFFFFF,t_70,g_se,x_16">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bf2piac4aaaqiamq5gjn5qfa6wdfz5aalqa.f10002.mp4?dis_k=9bd8c4db4d00cfec3d34e1635caee7be&dis_t=1652321385&spec_id=undefined1652321380&vid=wxv_1916836015676178436&format_id=10002&support_redirect=1&mmversion=false" type="video/mp4">
</video>

关于IT自动化和智能化，这个话题一直都在讨论，个人觉得自动化更注重于将多云(包含容器云)，devops, os/mw/database日常运维, 多任务批量调度，工单系统，多维可视化，多平台全链路安全监控日志告警等融合集成一体化，目标应该就是AllInOne的一体化运维平台，全链路监控，流程审批，安全审计以及开发、运维、项目管理等。既能适用于运维人员，也适用于开发和项目管理人员等。

IT智能化应该更偏向于单个具体产品的使用，比如数据库智能平台，能够将数据库运维的经验以及数据库监控指标相结合，通过多维度多场景实时监控数据库，发现异常能及时告警，常见的问题能够做到故障自愈，复杂的问题能给出具体判断点做到精准点位，而我们作为使用者只需要看看告警内容然后按下流程确定键，下一步后台就可以进行自动修复了。目标很明确，实现起来却是很难，需要有相关产品运维经验丰富的专家团队，运维开发团队以及大数据量、各种应用场景支撑测试验证等等。

待续......

