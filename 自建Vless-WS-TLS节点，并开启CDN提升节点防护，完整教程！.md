**请配合视频教程食用：https://youtu.be/eqYL6P6T9sU**
### VPS服务器购买
自建节点需要有一台VPS服务器，如想月付，可使用Vultr家的VPS服务器，[Vultr官网](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，目前月付3.5刀/月，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过32个机房可选，支持支付宝。<br />

如果追求极致速度，也可考虑使用搬瓦工VPS。[搬瓦工VPS官网](https://bwh88.net/aff.php?aff=71506)，以下是推荐用来自建节点的机房，可点链接直达。<br />[搬瓦工VPS订购、部署机器、服务器登录信息获取指引！](https://github.com/xiaochaib/chaiwiki/wiki/%E6%90%AC%E7%93%A6%E5%B7%A5VPS%E8%AE%A2%E8%B4%AD%E3%80%81%E9%83%A8%E7%BD%B2%E6%9C%BA%E5%99%A8%E3%80%81%E6%9C%8D%E5%8A%A1%E5%99%A8%E7%99%BB%E5%BD%95%E4%BF%A1%E6%81%AF%E8%8E%B7%E5%8F%96%E6%8C%87%E5%BC%95%EF%BC%81)
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
<td align="center">普通</td>
<td align="center">2 核</td>
<td align="center">1024 MB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">1 TB / 月</td>
<td align="center"><strong>$49.99 / 年</strong></td>
<td align="center"><a href="https://bwh88.net/aff.php?aff=71506&pid=44" rel="nofollow">购买</a></td>
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

### 域名购买、托管到CloudFlare
域名注册、购买，推荐使用namesilo，免费的whois隐私保护！<br />
NameSilo官网（域名）：[namesilo官网](https://www.namesilo.com/?rid=1cfe997de/)<br />
PING工具：[ping工具（检测解析域名是否生效）](https://ping.chinaz.com/)<br />
CloudFlare(套CDN)：[CF官网）](https://www.cloudflare.com/zh-cn/)

### # SSH连接工具
任选其中一个即可<br />
FinalShell(推荐、全平台):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)

# 安装V2Ray
### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y && apt install -y curl socat wget</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat wget

### 可选操作：部分VPS服务器需要开放端口（搬瓦工已默认开放所有端口,所以此步不需要）<br />
一些服务器的端口需要手动开放，像Vultr，需要安装防火墙（CentOS运行yum install firewalld安装）<br />
请参考此篇开放端口:[VPS开放端口](https://github.com/xiaochaib/chaiwiki/wiki/VPS%E5%BC%80%E6%94%BE%E7%AB%AF%E5%8F%A3%E5%B8%B8%E8%A7%84%E6%96%B9%E6%B3%95%EF%BC%81)

### 正式安装V2Ray(使用233Boy大佬的一键脚本)
系统支持：Ubuntu，Debian，CentOS，推荐使用 Ubuntu，谨慎使用 CentOS，脚本可能无法正常运行！<br />
执行如下命令：
<pre><code>bash <(wget -qO- -o- https://git.io/v2ray.sh)</pre></code>

# 管理面板
安装完成后，输入 v2ray 就能看到管理面板，如下图片所示
![image](https://github.com/xiaochaib/chaiwiki/assets/134616948/7fb98d7e-5063-4092-a00c-a22d3d4a7e7b)

V2Ray 脚本管理面板
提示，如果你不想执行任何功能，直接按 Enter 回车退出即可。

# BBR加速
四合一 BBR Plus / 原版BBR / 魔改BBR一键脚本（Centos 7, Debian 8/9, Ubuntu 16/18 测试通过）<br />
<pre><code>wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh</pre></code>

# 客户端下载
V2Ray-windows客户端：[v2rayN下载](https://github.com/2dust/v2rayN/releases)<br />
安卓：[V2RayNG](https://github.com/2dust/v2rayNG)<br />
苹果MAC OS：[V2RayU下载](https://github.com/yanue/V2rayU/releases)<br />
IOS：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）<br />
不管是iPad平板还是iPhone手机，比较推荐的科学上网软件必定是：Shadowrocket，但是需要注册一个非国区或美区账号才能进行购买，目前是2.99美刀约20块人民币，注册美区账号和充值购买也非常简单，请参考以下两篇文章。<br />
如何注册美区Apple ID:https://zhuanlan.zhihu.com/p/635054054<br />
美区账号如何充值：https://zhuanlan.zhihu.com/p/636121931<br />

# 结尾
一郑重声明：请合理使用科学上网于学习知识、外贸或科研工作方面，遵守相关规定<br />
搬瓦工30天内新账户支持退款，请按以下操作，refunds，按提示交工单，不懂英文的请打开浏览器翻译
![image](https://github.com/xiaochaib/chaiwiki/assets/134616948/2957ec12-85c0-4194-93f9-e06fe5e5bf88)

