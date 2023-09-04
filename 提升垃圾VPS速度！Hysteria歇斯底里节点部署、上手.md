请配合视频教程食用：https://www.youtube.com/@bigtouchai/playlists 视频有字幕，请打开字幕观看

# Hysteria介绍（摘自官方开源简介）
`Hysteria 是一个功能丰富的，专为恶劣网络环境进行优化的网络工具（双边加速），比如卫星网络、拥挤的公共 Wi-Fi、在中国连接国外服务器等。 基于修改版的 QUIC 协议。`

Hysteria这是一款由go编写的非常优秀的“轻量”代理程序，它很好的解决了在搭建富强魔法服务器时最大的痛点——线路拉跨。<br />
**用人话讲就是：提升垃圾VPS的上网速度、提升上网体验！**

# VPS服务器购买
自建节点的前提是需要有一台VPS服务器，如果已有购买到VPS服务器，此步可忽略，直接进入下一步的部署环节，如无，不知道哪家VPS好，可以选择以下推荐~<br />
1、推荐使用[搬瓦工（Bandwagon Host）](https://bwh88.net/aff.php?aff=71506)，非常稳定，不满意支持退款，不用担心跑路。
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
对于绝大多数用户来说，CN2线路已经满足；非常追求超极致速度、且有多人合租、钱包厚的朋友优先选择CN2 GIA或香港线路<br />
如果跳转到购买链接提示：Out of Stock说明没库存了，香港机一般很紧俏<br />
搬瓦工优惠码：**BWHNCXNVXV**<br />
----------------------------------------------------------------------<br />

2、或者Vultr家的VPS服务器，可使用Vultr家的VPS服务器，[Vultr官网](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，目前月付5刀/月，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过几十个机房可选，支持支付宝。<br />

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

# SSH连接工具
任选其中一个即可<br />
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)

# 正式部署Hysteria

### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y && apt install -y curl</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl

### 2、自签证书域名准备
要想使用自签证书，需要一串解析到你VPS的域名，请根据以下代码替换，将其中的10.0.0.1替换成你VPS服务器的真实IP地址，这一串就是对应你服务器的真实域名，并记录下来备用，下面部署时会用到这个域名
<pre><code>app.10.0.0.1.nip.io</pre></code>

### 3、安装Hysteria
感谢github FranzKafkaYu大佬开发如此好用的一键脚本
<pre><code>bash <(curl -fsSL https://git.io/hysteria.sh)</pre></code>


# 管理面板
安装完成后，输入 hihy 就能看到管理面板，如下图片所示，可以重新查看面板信息
<img width="1016" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/34f667da-3ede-4f6f-8c77-d00a90f53659">


# 客户端下载
[V2Ray官网对于全平台客户端的总结和一览](https://www.v2ray.com/awesome/tools.html)<br />

**Windows：**[v2rayN下载](https://github.com/2dust/v2rayN/releases)<br />

**苹果IOS、iPad**：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）<br />
不管是iPad平板还是iPhone手机，比较推荐的科学上网软件必定是：Shadowrocket，但是需要注册一个非国区或美区账号才能进行购买，目前是2.99美刀约20块人民币，注册美区账号和充值购买也非常简单，请参考以下两篇文章。<br />
如何注册美区Apple ID:https://zhuanlan.zhihu.com/p/635054054<br />
美区账号如何充值：https://zhuanlan.zhihu.com/p/636121931<br />
注册美区ID并按以上方法充值后，在App Store中搜索Shadowrocket购买并下载安装<br />

**安卓：**[V2RayNG](https://github.com/2dust/v2rayNG/releases)<br /><br />

**苹果MAC OS**：[V2RayU下载](https://github.com/yanue/V2rayU/releases)<br /><br />

# 结尾
一**请合理使用科学上网**<br />
搬瓦工30天内新账户支持退款，请按以下操作，refunds，按提示交工单，不懂英文的请打开浏览器翻译<br />
<img width="687" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/3f77af08-23ed-4a7d-809e-651bfa5537d9">



