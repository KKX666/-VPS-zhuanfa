# 搭建VPS国内转发
-------------------
怎样搭建vps国内转发
---------------------
本文脚本来自于https://github.com/arloor/iptablesUtils

感谢我金主大佬的手把手

第一步：购买国内中转vps

第二步：购买后映射一个内网端口和公网端口《公网端口30000-60000》内网随便

映射好后打开ssh软件  

第三步：ssh软件 IP填系统给你分配的公网IP和公网端口连接ssh

![image](https://user-images.githubusercontent.com/94978556/143914740-ed731a3a-aa37-4cee-9845-962cf7b9fa87.png)

第四步：安装转发脚本

`wget --no-check-certificate -qO natcfg.sh https://raw.githubusercontent.com/arloor/iptablesUtils/master/natcfg.sh && bash natcfg.sh`

如果不能安装自己谷歌自己找自己vps系统怎么装wget的方法
也可以试试以下两条

`yum install wget`

`wget --no-check-certificate -qO natcfg.sh http://www.arloor.com/sh/iptablesUtils/natcfg.sh && bash natcfg.sh`

第五步：安装好后选择`1`添加转发端口

第六步：输入你刚才自己映射的内网端口

![image](https://user-images.githubusercontent.com/94978556/143916304-f0d24dda-ae8b-4c81-befa-08c0ca0b0318.png)

第七步：输入你搭建好的v2ray节点端口

![image](https://user-images.githubusercontent.com/94978556/143916546-98386238-d559-46ec-9d6f-75e848a4e14d.png)

第八步：输入你搭建好的v2ray节点IP

![image](https://user-images.githubusercontent.com/94978556/143916720-3d4bfff3-8e66-4294-aecf-4f6559cb1745.png)

第九步：修改你的节点的IP和端口更换成你映射的公网IP和公网端口

以后还想加转发的话自己映射端口同理

想进入面板管理转发的话输入`bash natcfg.sh`

小提醒不要用192.168.xx.xx内网ip连接ssh哦 那是连接不上的

至此整个转发就OK啦
