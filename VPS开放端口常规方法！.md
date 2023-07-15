## 不少购买VPS服务器的朋友会遇到一个问题：默认只开放了SSH端口即22端口，但使用VPS搭建一些服务时会用到其它端口，如常规网站端口80、443等，以及一些其它服务需要开放其它端口，以下是常见开放端口的方法！
有两种，可按实际需求尝试：

方法1：iptables命令开放
开放命令，将80替换成你需要开放的端口
<pre><code>/sbin/iptables -I INPUT -p tcp --dport 80 -j ACCEPT</pre></code>
开放后，记得运行以下命令保存
<pre><code>/etc/rc.d/init.d/iptables save</pre></code>
保存后，重启服务生效
<pre><code>/etc/init.d/iptables restart</pre></code>

