**不少购买VPS服务器的朋友会遇到一个问题：默认只开放了SSH端口即22端口，但使用VPS搭建一些服务时会用到其它端口，如常规网站端口80、443等，以及一些其它服务需要开放其它端口，以下是常见开放端口的方法！**
有两种，可按实际需求尝试，因linux有许多发行版本，每个版本系统放行方式有所不同，以下仅作参考：如开放后导致无法连接ssh，请使用VPS后台的VNC界面连接操作

## 方法1：iptables命令开放
开放命令，将80替换成你需要开放的端口
<pre><code>/sbin/iptables -I INPUT -p tcp --dport 80 -j ACCEPT</pre></code>
开放后，记得运行以下命令保存
<pre><code>/etc/rc.d/init.d/iptables save</pre></code>
保存后，重启服务生效
<pre><code>/etc/init.d/iptables restart</pre></code>

## 方法2：防火墙开放
这种应该是最常用的，一般VPS服务器都有防火墙，如无，可运行安装，像Vultr，按官方文档就需要先安装防火墙，再开放端口<br />
运行以下命令安装防火墙（CentOS运行yum install firewalld安装）
<pre><code>apt-get install firewalld</pre></code>
然后复制以下命令，按需开放端口，将其中的22数字改成你需要开放的端口，运行命令即可生效，为防止连接上不SSH，第一条命令可先开放SSH端口
<pre><code>firewall-cmd --zone=public --add-port=22/tcp --permanent && firewall-cmd --reload</pre></code>

## ubuntu如何对外开放端口
１.查看已经开启的端口

<pre><code>sudo ufw status</pre></code>

2.打开端口，将其中80数字替换成你要放开的端口，有多个端口就运行多次

<pre><code>sudo ufw allow 80</pre></code>

3.开启防火墙

<pre><code>sudo ufw enable</pre></code>

４.重启防火墙

<pre><code>sudo ufw reload</pre></code>

5.再次查看一下端口是否已开放，即运行第一条命令，有显示你要的端口即代表已放开
<img width="568" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/84ddb3d2-43fb-4fb4-9688-6312bbb3622b">



