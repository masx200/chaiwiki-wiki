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
对于绝大多数用户来说，CN2线路已经满足；非常追求超极致速度、钱包厚的朋友可以选择CN2 GIA或香港线路，支持支付宝<br />
搬瓦工优惠码：**BWHNCXNVXV**

### 域名购买、托管
可使用Goday：[官网](https://www.godaddy.com/)或namesilo等域名注册商购买域名，推荐使用namesilo，免费的whois隐私保护！<br />
NameSilo官网：[namesilo官网](https://www.namesilo.com/?rid=1cfe997de/)<br />
namesilo优惠码：**idcspy2020**<br />
将域名托管到CloudFlare，方便后续开启CDN中转
CloudFlare官网：[CloudFlare官网](https://www.cloudflare.com)<br />

### # SSH连接工具
任选其中一个即可<br />
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)

### 安装Trojan（自带伪装网站）
### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y && apt install -y curl socat wget</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat wget

### 如果是Vultr，需要开放端口
Vultr目前机器只默认开放SSH端口22，其它一些端口全部需要手动开放，复制以下命令运行就行

<pre><code>apt-get install firewalld -y && firewall-cmd --zone=public --add-port=443/tcp --permanent && firewall-cmd --zone=public --add-port=80/tcp --permanent && firewall-cmd --reload</pre></code>

### 2、申请证书
[ping工具（检测解析域名是否生效）](https://ping.chinaz.com/)<br />
首先需要申请证书
安装Acme
<pre><code>curl https://get.acme.sh | sh</pre></code>
“你的邮箱”改成你的邮箱地址
<pre><code>~/.acme.sh/acme.sh --register-account -m 你的邮箱</pre></code>
“你的域名”改成你前面解析好的域名
<pre><code>~/.acme.sh/acme.sh --issue -d 你的域名 --standalone</pre></code>
正式安装Trojan
<pre><code>curl -O https://raw.githubusercontent.com/xiaochaib/trojan_atrandys/edit/trojan_mult.sh && chmod +x trojan_mult.sh && ./trojan_mult.sh</pre></code>

### 获取Trojan配置信息
复制以下路径到FinalSheel中访问，找到server.conf直接在FinalShell中打开
<pre><code>/usr/src/trojan</pre></code>
如需要更改密码，修改server.conf后重新上传，再运行以下命令重启trojan生效
<pre><code>systemctl restart trojan</pre></code>

# BBR加速
四合一 BBR Plus / 原版BBR / 魔改BBR一键脚本（Centos 7, Debian 8/9, Ubuntu 16/18 测试通过）<br />
<pre><code>wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh</pre></code>

# 客户端下载
Trojan-windows客户端：[v2rayN下载](https://github.com/2dust/v2rayN/releases)<br />
IOS：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）<br />
安卓：[igniter](https://github.com/trojan-gfw/igniter/releases)<br />
苹果MAC OS：[V2RayU下载](https://github.com/yanue/V2rayU/releases)<br />
