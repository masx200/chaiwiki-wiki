请配合视频教程食用：https://youtu.be/AqfhmqC5HWI
# 前言
借助x-ui面板可以部署V2Ray、Xray、SS、Trojan等协议的节点，并且有后台面板方便查看和设置节点信息，对小白非常友好，请结合以下步骤进行操作。


# VPS服务器购买
自建节点的前提是需要有一台VPS服务器，推荐使用[搬瓦工（Bandwagon Host）](https://bwh88.net/aff.php?aff=71506)，非常稳定，不满意支持退款，不用担心跑路。[搬瓦工VPS订购、部署机器、服务器登录信息获取指引！](https://github.com/xiaochaib/chaiwiki/wiki/%E6%90%AC%E7%93%A6%E5%B7%A5VPS%E8%AE%A2%E8%B4%AD%E3%80%81%E9%83%A8%E7%BD%B2%E6%9C%BA%E5%99%A8%E3%80%81%E6%9C%8D%E5%8A%A1%E5%99%A8%E7%99%BB%E5%BD%95%E4%BF%A1%E6%81%AF%E8%8E%B7%E5%8F%96%E6%8C%87%E5%BC%95%EF%BC%81)
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

# 域名购买、解析
可使用Goday：[官网](https://www.godaddy.com/)或namesilo等域名注册商购买域名，推荐使用namesilo，免费的whois隐私保护！<br />
NameSilo官网：[namesilo官网](https://www.namesilo.com/?rid=1cfe997de/)<br />
namesilo优惠码：**idcspy2020**

# SSH连接工具
任选其中一个即可<br />
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)

# 正式安装、搭建节点

### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y</pre></code>
<pre><code>apt install -y curl socat wget</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat wget


### 2、安装x-ui
感谢github vaxilu大佬开发如此好用的一键脚本
<pre><code>bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)</pre></code>

### 3、证书申请（开TLS提升安全性必备）
[ping工具（检测解析域名是否生效）](https://ping.chinaz.com/)<br />
安装Acme
<pre><code>curl https://get.acme.sh | sh</pre></code>
“你的邮箱”改成你的邮箱地址
<pre><code>~/.acme.sh/acme.sh --register-account -m 你的邮箱</pre></code>
“你的域名”改成你前面解析好的域名
<pre><code>~/.acme.sh/acme.sh --issue -d 你的域名 --standalone</pre></code>

# BBR加速
四合一 BBR Plus / 原版BBR / 魔改BBR一键脚本（Centos 7, Debian 8/9, Ubuntu 16/18 测试通过）<br />
<pre><code>wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh</pre></code>


# 客户端下载
[V2Ray官网对于全平台客户端的总结和一览](https://www.v2ray.com/awesome/tools.html)<br />

**Windows：**[v2rayN下载](https://github.com/2dust/v2rayN/releases)<br />
**IOS：**App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）<br />
不管是iPad平板还是iPhone手机，比较推荐的科学上网软件必定是：Shadowrocket，但是需要注册一个非国区或美区账号才能进行购买，目前是2.99美刀约20块人民币，注册美区账号和充值购买也非常简单，请参考以下两篇文章。<br />
如何注册美区Apple ID:https://zhuanlan.zhihu.com/p/635054054<br />
美区账号如何充值：https://zhuanlan.zhihu.com/p/636121931<br />
**安卓：**[V2RayNG](https://github.com/2dust/v2rayNG/releases)<br />
**苹果MAC OS**：[V2RayU下载](https://github.com/yanue/V2rayU/releases)<br />

# 结尾
一**请合理使用科学上网，遵守所在地规定,请勿使用在不当地方**<br />
搬瓦工30天内新账户支持退款，请按以下操作，refunds，按提示交工单，不懂英文的请打开浏览器翻译<br />
<img width="687" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/3f77af08-23ed-4a7d-809e-651bfa5537d9">

