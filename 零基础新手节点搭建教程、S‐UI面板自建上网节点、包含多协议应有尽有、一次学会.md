# 前言
零基础部署V2Ray（Vmess+Vless）、Xray、SS、Trojan、reality、Hysteria(1+2)、Naive、TUIC、XTLS等协议的节点，并且有后台面板方便查看和设置节点信息，对小白非常友好，请结合以下步骤进行操作。


# VPS服务器购买
自建节点的前提是需要有一台VPS服务器，推荐使用[搬瓦工（Bandwagon Host）](https://bwh88.net/aff.php?aff=71506)，非常稳定，不满意支持退款，不用担心跑路。
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
<td align="center">性价比</td>
<td align="center">2 核</td>
<td align="center">1024 MB</td>
<td align="center">20 GB</td>
<td align="center">1 G</td>
<td align="center">1 TB / 月</td>
<td align="center"><strong>$49.99 / 年</strong></td>
<td align="center"><a href="https://bwh88.net/aff.php?aff=71506&pid=44" rel="nofollow">购买</a></td>
</tr>
<tr>
<td align="center">CN2 GIA高端</td>
<td align="center">2 核</td>
<td align="center">1 GB</td>
<td align="center">20 GB</td>
<td align="center"><strong>2.5 G</strong></td>
<td align="center">1000GB / 月</td>
<td align="center"><strong>$49.99 / 季 or $169.99 / 年</strong></td>
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
对于绝大多数用户来说，CN2线路已经满足；非常追求超极致速度、且有多人合租、钱包厚的朋友优先选择CN2 GIA或香港线路<br />
如果跳转到购买链接提示：Out of Stock说明没库存了，香港机一般很紧俏<br />
搬瓦工优惠码：**BWHCGLUKKB**


如果真的不想自建，想用机场，那么我推荐你使用搬瓦工官方JMS机场，非常稳定、不跑路！<br />
[搬瓦工JMS机场使用图文指引！点我~](https://github.com/bigtouchai/chaiwiki/wiki/%E6%9C%80%E7%A8%B3%E6%9C%BA%E5%9C%BA%EF%BC%9A%E6%90%AC%E7%93%A6%E5%B7%A5Just-My-Socks-%E6%9C%BA%E5%9C%BA%E5%A6%82%E4%BD%95%E8%B4%AD%E4%B9%B0%E4%BD%BF%E7%94%A8%E3%80%81%E5%A6%82%E4%BD%95%E9%85%8D%E7%BD%AE%E5%AE%A2%E6%88%B7%E7%AB%AF)

# SSH连接工具
任选其中一个即可<br />
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)

# S-UI面板+节点部署

### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y && apt install -y curl socat wget</pre></code>
**注意：**如果是centos系统，则运行yum update -y && yum install -y curl socat wget


### 2、安装S-UI
感谢alireza0大佬开发如此好用的安装脚本
<pre><code>VERSION=1.3.6 && bash <(curl -Ls https://raw.githubusercontent.com/alireza0/s-ui/$VERSION/install.sh) $VERSION</pre></code>

### 3、挑选SNI伪装域名（任选一个）
<pre><code>
aws.com
www.bing.com
snap.licdn.com
devblogs.microsoft.com
cdn.bizibly.com
www.apple.com
ts1.tc.mm.bing.net
fpinit.itunes.apple.com
go.microsoft.com
catalog.gamepass.com
gray-config-prod.api.arc-cdn.net
apps.mzstatic.com
tag.demandbase.com
r.bing.com
tag-logger.demandbase.com
cdn-dynmedia-1.microsoft.com
services.digitaleast.mobi
gray.video-player.arcpublishing.com
azure.microsoft.com
beacon.gtv-pub.com
amd.com
</pre></code>

# 面板管理、BBR加速
安装完成后，输入 s-ui 就能看到管理面板，如下图片所示，可以重新查看面板信息<br />
<img width="770" alt="image" src="https://github.com/user-attachments/assets/a45cc734-a388-4690-99e3-e2eef30fad91"><br />


重新获取SUI后台访问地址，可输入s-ui运行，再次输入10运行，查看面板参数来确定面板后台地址、管理员登录信息：<br />
<img width="501" height="348" alt="image" src="https://github.com/user-attachments/assets/90637ad1-d958-4253-97e8-76247919b744" />


### BBR加速
输入s-ui运行，输入18运行，输入1运行，开启BBR加速，显著提升速度
<img width="507" height="138" alt="image" src="https://github.com/user-attachments/assets/bf384751-b586-4688-bae8-9731aa4c48bb" />


# 各平台客户端下载
[V2Ray官网对于全平台客户端的总结和一览](https://www.v2ray.com/awesome/tools.html)<br />


**Windows、MacBook：**[v2rayN下载](https://github.com/2dust/v2rayN/releases/tag/7.14.12)<br />
**[解压软件winrar](https://www.winrar.com.cn/)<br />

**MacBook打开软件提示损坏解决方法：**[MacBook打开软件提示损坏解决方法](https://zhuanlan.zhihu.com/p/135948430)<br />
**MacBook打开软件提示无法验证软件安全性：**[MacBook打开软件提示无法验证安全性解决方法](https://zhuanlan.zhihu.com/p/489710134)<br />

**苹果IOS、iPad、M芯片MacBook**：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）<br />
不管是iPad平板还是iPhone手机，比较推荐的科学上网软件必定是：Shadowrocket，但是需要注册一个非国区或美区账号才能进行购买，目前是2.99美刀约20块人民币，注册美区账号和充值购买也非常简单，请参考以下两篇文章。<br />
如何注册美区Apple ID:https://zhuanlan.zhihu.com/p/30761252365<br />
美区账号如何充值：https://zhuanlan.zhihu.com/p/636121931<br />
注册美区ID并按以上方法充值后，在App Store中搜索Shadowrocket购买并下载安装<br />

**安卓/Android：**[NekoBox下载](https://github.com/MatsuriDayo/NekoBoxForAndroid/releases/tag/1.4.0)<br />

# 结尾
一**郑重声明：请合理使用科学上网于学习知识、外贸或科研工作方面，遵守当地相关规定**<br />
搬瓦工30天内新账户支持退款，请按以下操作，refunds，按提示交工单，不懂英文的请打开浏览器翻译<br />
<img width="687" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/3f77af08-23ed-4a7d-809e-651bfa5537d9">

