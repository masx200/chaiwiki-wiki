### VPS服务器购买
自建节点需要有一台VPS服务器，如想月付，可使用Vultr家的VPS服务器，[Vultr官网](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，目前月付3.5刀/月，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过32个机房可选，支持支付宝。<br />

如果追求极致速度，也可考虑使用搬瓦工VPS。[搬瓦工VPS官网](https://bwh88.net/aff.php?aff=71506)，以下是推荐用来自建节点的机房，可点链接直达。<table role="table">
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
<td align="center">CN2</td>
<td align="center">1 核</td>
<td align="center">1024 MB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">1000GB / 月</td>
<td align="center"><strong>$49.99 / 年</strong></td>
<td align="center"><a href="https://bwh88.net/aff.php?aff=71506&pid=57" rel="nofollow">购买</a></td>
</tr>
<tr>
<td align="center">CN2 GIA</td>
<td align="center">2 核</td>
<td align="center">1 GB</td>
<td align="center">20 GB</td>
<td align="center"><strong>2.5 G</strong></td>
<td align="center">1000GB / 月</td>
<td align="center"><strong>$49.99 / 季</strong></td>
<td align="center"><a href="https://bwh88.net/aff.php?aff=71506&pid=87" rel="nofollow">购买</a></td>
</tr>
<tr>
<td align="center">香港</td>
<td align="center">2 核</td>
<td align="center">2048 MB</td>
<td align="center">40 GB</td>
<td align="center">1 G</td>
<td align="center">500GB / 月</td>
<td align="center"><strong>$89.99 / 月</strong></td>
<td align="center"><a href="https://bwh88.net/aff.php?aff=71506&pid=95" rel="nofollow">购买</a></td>
</tr>
</tbody>
</table>
对于绝大多数用户来说，CN2线路已经满足；非常追求超极致速度、钱包厚的朋友可以选择CN2 GIA或香港线路<br />
如果跳转到购买链接提示：Out of Stock说明没库存了，香港机一般很紧俏<br />
搬瓦工优惠码：**BWHNCXNVXV**


如果真的不想自建，想用机场，那么我推荐你使用搬瓦工官方JMS机场，非常稳定、不跑路！<br />
[搬瓦工JMS机场使用图文指引！点我~](https://github.com/bigtouchai/chaiwiki/wiki/%E6%9C%80%E7%A8%B3%E6%9C%BA%E5%9C%BA%EF%BC%9A%E6%90%AC%E7%93%A6%E5%B7%A5Just-My-Socks-%E6%9C%BA%E5%9C%BA%E5%A6%82%E4%BD%95%E8%B4%AD%E4%B9%B0%E4%BD%BF%E7%94%A8%E3%80%81%E5%A6%82%E4%BD%95%E9%85%8D%E7%BD%AE%E5%AE%A2%E6%88%B7%E7%AB%AF)


### # SSH连接工具
任选其中一个即可<br />
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)<br />
检测VPS的IP是否通畅：
PING工具：[ping工具](https://ping.chinaz.com/)

# 使用XRay一键脚本安装V2Ray+Reality协议
### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y && apt install -y curl socat wget</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat wget

### 如果是Vultr，需要开放端口
Vultr目前机器只默认开放SSH端口22，其它一些端口全部需要手动开放，复制以下命令运行就行

<pre><code>apt-get install firewalld -y && firewall-cmd --zone=public --add-port=443/tcp --permanent && firewall-cmd --zone=public --add-port=80/tcp --permanent && firewall-cmd --zone=public --add-port=22/tcp --permanent && firewall-cmd --reload</pre></code>

### 正式安装XRay并部署V2Ray+Reality节点(使用233Boy大佬的一键脚本)
系统支持：Ubuntu，Debian，CentOS，推荐使用 Ubuntu，谨慎使用 CentOS，脚本可能无法正常运行！<br />
执行如下命令：
<pre><code>bash <(wget -qO- -o- https://github.com/233boy/Xray/raw/main/install.sh) -v v1.8.3</pre></code>

# 管理面板
安装完成后，输入 xray 就能看到管理面板，如下图片所示
![image](https://github.com/xiaochaib/chaiwiki/assets/134616948/a469a055-dad9-403c-8616-e25558ece040)


V2Ray 脚本管理面板
提示，如果你不想执行任何功能，直接按 Enter 回车退出即可。

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

