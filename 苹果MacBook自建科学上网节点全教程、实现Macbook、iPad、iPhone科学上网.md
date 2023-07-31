请配合视频教程食用：
# 前言
许多朋友是使用苹果全家桶的，但网上许多搭建节点的教程都是在Windows系统上演示的，单纯使用MacBook电脑来演示搭建全程的教程非常少，所以这期视频我会演示如何在苹果MacBook电脑上自建节点、以及如何在MacBook、苹果iPhone、iPad平板上使用自建的节点进行科学上网，最后，有些主力使用苹果全家桶的朋友可能也会有Windows电脑或安卓手机，所以也会演示如何在Windows、安卓手机上使用这些节点进行科学上网。

这期苹果MacBook自建节点的教程我会尽量精简操作步骤，如果是零基础的朋友也不用担心，跟着我的步骤，肯定可以搭建成功的。
自建科学上网节点的首要前提是要购买一台国外的VPS服务器，购买服务器之后，就可以搭建个人专属的科学上网节点了。


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


# SSH连接工具
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />


# 正式安装、搭建节点

### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y && apt install -y curl wget</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat wget


### 2、安装x-ui
感谢github FranzKafkaYu大佬开发如此好用的一键脚本
<pre><code>bash <(curl -Ls https://raw.githubusercontent.com/FranzKafkaYu/x-ui/master/install.sh)</pre></code>


# BBR加速
内置bbr加速，输入x-ui显示菜单，输入数字15即可自动一键安装bbr加速，提升科学上网速度。<br />
<img width="736" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/97af6a16-230f-48c2-a217-5469e85113f2">

或者使用以下脚本安装bbr：
四合一 BBR Plus / 原版BBR / 魔改BBR一键脚本（Centos 7, Debian 8/9, Ubuntu 16/18 测试通过）<br />
<pre><code>wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh</pre></code>


# 客户端下载
[V2Ray官网对于全平台客户端的总结和一览](https://www.v2ray.com/awesome/tools.html)<br />

不管是iPad平板还是iPhone手机，比较推荐的科学上网软件必定是：Shadowrocket，但是需要注册一个非国区或美区账号才能进行购买，目前是2.99美刀约20块人民币，注册美区账号和充值购买也非常简单，请参考以下两篇文章。<br />
如何注册美区Apple ID:https://zhuanlan.zhihu.com/p/635054054<br />
美区账号如何充值：https://zhuanlan.zhihu.com/p/636121931<br />

在App Store登录你注册的美区ID并充值3刀后，直接在App Store搜索Shadowrocket，就可以完成购买并下载。<br />

如果是MacBook电脑，推荐使用V2RayU客户端，支持协议也非常全面。<br />
苹果MAC OS：[V2RayU下载](https://github.com/yanue/V2rayU/releases)<br />

恰好，如果手上也有Windows系统或安卓手机需要使用科学上网，那么它们的客户端下载链接分别如下：<br />
Windows：[v2rayN下载](https://github.com/2dust/v2rayN/releases)<br />
安卓：[V2RayNG](https://github.com/2dust/v2rayNG/releases)<br />


# 结尾
一**请合理使用科学上网**<br />
搬瓦工30天内新账户支持退款，请按以下操作，refunds，按提示交工单，不懂英文的请打开浏览器翻译<br />
<img width="687" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/3f77af08-23ed-4a7d-809e-651bfa5537d9">

