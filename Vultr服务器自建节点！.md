### Vultr服务器购买
自建节点需要有一台VPS服务器，本次推荐[Vultr（官网）](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳。<br />



### Vultr开放端口
Vultr目前机器只默认开放SSH端口22，其它一些端口全部需要手动开放。
<pre><code>apt-get install firewalld -y</pre></code>
443处替换成你需要开放的端口号
<pre><code>firewall-cmd --zone=public --add-port=443/tcp --permanent</pre></code>
每次新开放端口后，重启防火墙
<pre><code>firewall-cmd --reload</pre></code>
