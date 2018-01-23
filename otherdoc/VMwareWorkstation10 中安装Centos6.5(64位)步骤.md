---
title: VMwareWorkstation10 安装Centos6.5(64位)步骤图文版
tags:VMwareWorkstation,Centos6.5
grammar_cjkRuby: true
---


1. 点击“新建虚拟机”，到向导窗口。选择自定义—>下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos01.jpg)
2. 选择虚拟机硬件兼容workstation10.0，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos02.png)
3. 选择稍后安装系统，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos03.png)
4. 选择操作系统为Linux,版本CentOS 64 位。下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos04.png)
5. 给虚拟机命名，指定安装位置，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos05.png)
6. 配置处理器信息（我这里采用默认），下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos06.png)
7. 配置内存信息（我这里采用默认信息），下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos07.png)
8. 配置网络信息，(建议采用桥连或仅主机模式)，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos08.png)
9. 选择I/O类型（默认设置），下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos09.png)
10. 选择磁盘类型（默认），下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos10.png)
11. 选择创建新磁盘，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos11.png)
12. 配置磁盘大小，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos12.png)
13. 不用改动，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos13.png)
14. 配置成功，完成。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos14.png)
15. 如果对刚才的配置需要更改，点击workstation的编辑虚拟机设置，进行更改。在这里我们要指定Centos镜像文件的位置，并勾选启动时链接。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos15.png)
16. 点击workstation的 开启此虚拟机。进入Centos的安装窗口。选择安装系统（第一个第二个都可以），回车。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos16.png)
17. 选择跳过，回车。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos17.png)
18. 点击下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos18.png)
19. 选择English(为防止兼容性问题，建议选择English),下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos19.png)
20. 选择U.S English，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos20.png)
21. 选择 基本的存储设备，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos21.png)
22. 选择格式化数据，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos22.png)
23. 命名Hostname，配置网络连接ConfigureNetwork.选择Connect automatically,自动连接。下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos23-1.png)
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos23-2.png)
24. 选择时区，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos24.png)
25. 给root用户设置密码，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos25.png)
26. 默认设置，下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos26.png)
27. 选择Destop,下一步。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos27.png)
28. 开始安装，等待安装结束。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos28.png)
29. 安装完成，点击重启。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos29.png)
30. 配置用户信息，下一步，完成重启，Centos安装完毕。
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos30-1.png)
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos30-2.png)
![](http://www.smartleon.net/wp-content/uploads/2017/12/vmarecentos30-3.png)
至此，Centos 就安装完毕了。