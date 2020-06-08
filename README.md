# RemoteApp
# 环境要求：
CPU:最低2.0GHz处理器

内存:最低4G

显卡:核显以上

操作系统:windows 7 x64及以上

软件有效期:30天

# 部署方式
场景1：跳板机模式，编码和转发全部在本机完成，本机承担了所有的计算和编码任务，远程计算机只作为服务器来使用，可以使用桌面。

场景2：一体机模式，编码和转发全部再远程完成，本机只需要打开浏览器即可，但是在远程计算机不支持多人登录的情况下（可破解），不能打开桌面，应用打开不受影响。

![screenshot1](https://github.com/Niap/RemoteAppWebsite/raw/master/frame.png)

# 部署步骤
0. 关闭防火墙

打开控制面板->windows防火墙。

1. 开启远程桌面

打开控制面板->系统，点击远程设置，选择允许运行任意版本远程桌面的计算机连接。

注意：开启远程桌面必须要设置windows的账户密码，尽量设置电脑为不睡眠状态。

![screenshot1](https://github.com/Niap/RemoteAppWebsite/raw/master/shot1.png)

2. 安装.netframework 4.0及以上和RemoteAppTool

因为RemoteAppTool需要安装.netframework 4.0以上，如果不安装，则会报以下错误

![screenshot2](https://github.com/Niap/RemoteAppWebsite/raw/master/shot2.png)

3. 使用RemoteAppTool发布一个应用，这里以nodepad为例

点击左下角，添加，找到notepad所在的位置，选中notepad后，软件会自动发布notepad。

![screenshot3](https://github.com/Niap/RemoteAppWebsite/raw/master/shot3.png)
![screenshot4](https://github.com/Niap/RemoteAppWebsite/raw/master/shot4.png)

发布后界面为，双击“记事本”，修改Name和Full name为英文，这里修改成notepad即可。

![screenshot5](https://github.com/Niap/RemoteAppWebsite/raw/master/shot5.png)

4. 安装RemoteApp.js

点击安装Microsoft visual c++ 2005 redistributable 14.0(vc_redist.x64.exe)

解压pkg-win，双击remoteapp.exe，出现以下界面表示运行成功，期间可能弹出加入防火墙的提醒，点击确定即可。

![screenshot6](https://github.com/Niap/RemoteAppWebsite/raw/master/shot6.png)

5. 用另外一台电脑访问 http://当前电脑ip:9999 ，例如 http://192.168.0.110:9999

![screenshot7](https://github.com/Niap/RemoteAppWebsite/raw/master/shot7.png)

点击设置后，设置主机ip，端口，用户名和密码，这里ip地址设置为127.0.0.1，用户名密码设置为windows登陆的账号名密码。

6. 发布网页端应用

点击添加,输入刚刚在发布工具中修改的name和full name，并上传一个图标，点击保存后，再点开刚刚发布的应用等待一段时间即可打开。

![screenshot8](https://github.com/Niap/RemoteAppWebsite/raw/master/shot8.png)

