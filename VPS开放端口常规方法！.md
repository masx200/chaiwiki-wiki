**不少购买VPS服务器的朋友会遇到一个问题：默认只开放了SSH端口即22端口，但使用VPS搭建一些服务时会用到其它端口，如常规网站端口80、443等，以及一些其它服务需要开放其它端口，以下是常见开放端口的方法！**
有两种，可按实际需求尝试，因linux有许多发行版本，每个版本系统放行方式有所不同，以下仅作参考：

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

