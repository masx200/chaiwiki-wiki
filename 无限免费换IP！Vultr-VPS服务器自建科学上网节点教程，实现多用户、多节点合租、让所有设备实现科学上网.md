请配合视频教程食用：https://youtu.be/d3rhbK4ZHIw
### VPS服务器购买
自建节点需要有一台VPS服务器，如想月付，可使用Vultr家的VPS服务器，[Vultr官网](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，目前月付3.5刀/月，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过32个机房可选，支持支付宝。<br />

<table role="table">
<thead>
<tr>
<th align="center">线路名称</th>
<th align="center">处理器</th>
<th align="center">内存大小</th>
<th align="center">硬盘容量</th>
<th align="center">带宽</th>
<th align="center">流量</th>
<th align="center">价格</th>
<th align="center">链接</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">Vultr-入门</td>
<td align="center">1 核</td>
<td align="center">1024 MB</td>
<td align="center">25 GB</td>
<td align="center">1 G</td>
<td align="center">1024GB / 月</td>
<td align="center"><strong>$5 / 月</strong></td>
<td align="center"><a href="https://www.vultr.com/?ref=9467366" rel="nofollow">购买</a></td>
</tr>
<tr>
<td align="center">Vultr-进阶</td>
<td align="center">1 核</td>
<td align="center">2048 MB</td>
<td align="center">55 GB</td>
<td align="center">1 G</td>
<td align="center">2048GB / 月</td>
<td align="center"><strong>$10 / 月</strong></td>
<td align="center"><a href="https://www.vultr.com/?ref=9467366" rel="nofollow">购买</a></td>
</tr>
</tbody>
</table>
对于绝大多数用户来说，入门线路已经满足，5美刀一个月，并且每月1TB流量，适合多人使用，可以和朋友合租一起用；<br />


如果真的不想自建，想用机场，那么我推荐你使用搬瓦工官方JMS机场，非常稳定、不跑路！<br />
[搬瓦工JMS机场使用图文指引！点我~](https://github.com/bigtouchai/chaiwiki/wiki/%E6%9C%80%E7%A8%B3%E6%9C%BA%E5%9C%BA%EF%BC%9A%E6%90%AC%E7%93%A6%E5%B7%A5Just-My-Socks-%E6%9C%BA%E5%9C%BA%E5%A6%82%E4%BD%95%E8%B4%AD%E4%B9%B0%E4%BD%BF%E7%94%A8%E3%80%81%E5%A6%82%E4%BD%95%E9%85%8D%E7%BD%AE%E5%AE%A2%E6%88%B7%E7%AB%AF)

### 检测服务器状态
Vultr VPS服务器开通后，有机率会分配到被墙的IP，但胜在Vultr是按时计费的，所以可以随时销毁机器进行新IP分配（新建的机器要5分钟后才能执行销毁）。<br />

机器开通后大概3-5分钟（一定要3-5分钟后再检测，刚新建的机器初始化中），复制机器的IP到以下网址进行ping检测，如可以检测通过就代表这个IP可用，否则，销毁机器，按前面新建机器的步骤重新来一次，再检测IP，直到IP可用。
PING工具：[ping工具（检测服务器IP是否可用）](https://ping.chinaz.com/)


### # SSH连接工具
任选其中一个即可<br />
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)


### 安装X-ui面板并配置节点
### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y && apt install -y curl wget</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat wget


### 2、安装x-ui
感谢github FranzKafkaYu大佬开发如此好用的一键脚本
<pre><code>bash <(curl -Ls https://raw.githubusercontent.com/FranzKafkaYu/x-ui/master/install.sh)</pre></code>

### 手动开放端口
Vultr目前机器只默认开放SSH端口22，其它一些端口全部需要手动开放，依次复制以下命令运行就行<br />
首先，需要安装防火墙，复制以下命令到ssh中运行就行
<pre><code>apt-get install firewalld -y && firewall-cmd --zone=public --add-port=22/tcp --permanent && firewall-cmd --reload</pre></code>

根据你获取的节点信息，记下节点信息中的端口（port）号，将记下的端口号替换到下方命令中的『端口』两字中，即是完整命令，运行即可、当然，x-ui面板的端口首先要开放
<pre><code>firewall-cmd --zone=public --add-port=端口/tcp --permanent && firewall-cmd --reload</pre></code>
注意，后续如果重新配置节点信息，端口有变动，切记重新运行以上放行端口的命令，不然会导致节点无法使用，切记

参考Vultr官方文档对于放行端口的说明：https://www.vultr.com/docs/firewall-quickstart-for-vultr-cloud-servers/


# 管理面板
安装完成后，输入 x-ui 就能看到管理面板，如下图片所示，可以重新查看面板信息
<img width="770" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/879a01cc-f20b-4efb-bc35-5710bbddcf7d">


# BBR加速
四合一 BBR Plus / 原版BBR / 魔改BBR一键脚本（Centos 7, Debian 8/9, Ubuntu 16/18 测试通过）<br />
<pre><code>wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh</pre></code>


# 客户端下载
V2Ray-windows客户端：[v2rayN下载](https://github.com/2dust/v2rayN/releases)<br />
IOS：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）<br />
安卓：[V2RayNG](https://github.com/2dust/v2rayNG)<br />
苹果MAC OS：[V2RayU下载](https://github.com/yanue/V2rayU/releases)<br />

# 结尾
一请合理使用科学上网<br />
搬瓦工30天内新账户支持退款，请按以下操作，refunds，按提示交工单，不懂英文的请打开浏览器翻译
![image](https://github.com/xiaochaib/chaiwiki/assets/134616948/2957ec12-85c0-4194-93f9-e06fe5e5bf88)

