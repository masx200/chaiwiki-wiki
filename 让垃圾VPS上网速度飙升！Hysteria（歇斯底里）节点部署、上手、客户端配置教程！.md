请配合视频教程食用：https://youtu.be/-CF5wZocHXM 视频有字幕，请打开字幕观看

# Hysteria介绍（摘自官方开源简介）
`Hysteria 是一个功能丰富的，专为恶劣网络环境进行优化的网络工具（双边加速），比如卫星网络、拥挤的公共 Wi-Fi、在中国连接国外服务器等。 基于修改版的 QUIC 协议。`

Hysteria这是一款由go编写的非常优秀的“轻量”代理程序，它很好的解决了在搭建富强魔法服务器时最大的痛点——线路拉跨。<br />
**用人话讲就是：提升垃圾VPS的上网速度、提升上网体验！**

# VPS服务器购买
自建节点的前提是需要有一台VPS服务器，如果已有购买到VPS服务器，此步可忽略，直接进入下一步的部署环节，如无，不知道哪家VPS好，可以选择以下推荐~<br />
1、推荐使用[搬瓦工（Bandwagon Host）](https://bwh88.net/aff.php?aff=71506)，非常稳定，不满意支持退款，不用担心跑路。<br />
[搬瓦工VPS订购、部署机器、服务器登录信息获取指引！](https://github.com/xiaochaib/chaiwiki/wiki/%E6%90%AC%E7%93%A6%E5%B7%A5VPS%E8%AE%A2%E8%B4%AD%E3%80%81%E9%83%A8%E7%BD%B2%E6%9C%BA%E5%99%A8%E3%80%81%E6%9C%8D%E5%8A%A1%E5%99%A8%E7%99%BB%E5%BD%95%E4%BF%A1%E6%81%AF%E8%8E%B7%E5%8F%96%E6%8C%87%E5%BC%95%EF%BC%81)
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
对于绝大多数用户来说，CN2线路已经满足；非常追求超极致速度、且有多人合租、钱包厚的朋友优先选择CN2 GIA或香港线路<br />
如果跳转到购买链接提示：Out of Stock说明没库存了，香港机一般很紧俏<br />
搬瓦工优惠码：**BWHCGLUKKB**<br />
----------------------------------------------------------------------<br />

2、或者Vultr家的VPS服务器，可使用Vultr家的VPS服务器，[Vultr官网](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，目前月付5刀/月，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过几十个机房可选，支持支付宝。<br />
[Vultr VPS订购、部署机器、服务器登录信息获取指引！](https://github.com/xiaochaib/chaiwiki/wiki/Vultr-VPS%E8%AE%A2%E8%B4%AD%E3%80%81%E9%83%A8%E7%BD%B2%E6%9C%BA%E5%99%A8%E3%80%81%E6%9C%8D%E5%8A%A1%E5%99%A8%E7%99%BB%E5%BD%95%E4%BF%A1%E6%81%AF%E8%8E%B7%E5%8F%96%E6%8C%87%E5%BC%95%EF%BC%81)

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

### 2、证书域名准备（acme申请证书必须）
要想使用acme证书，需要一串解析到你VPS的域名，请根据以下代码替换，将其中的10.0.0.1替换成你VPS服务器的真实IP地址，这一串就是对应你服务器的真实域名，并记录下来备用，下面部署时会用到这个域名
<pre><code>app.10.0.0.1.nip.io</pre></code>

### 3、安装Hysteria
虽然脚本默认会放开所需端口，但有些VPS服务商可能要手动开启相关端口，如80/443端口必须要安装以下脚本前确认是开放状态，否则会失败<br />
此处默认你已放开所需端口，如未放开80/443端口，安装时会提示以下错误，如有此提示，请参考下方放行端口教程，或谷歌搜索你系统加+端口放行 关键字查询如何放行端口<br />
<img width="622" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/5cdb63f8-361f-4e40-b831-11feaa860ba2">

[放行端口参考教程](https://github.com/xiaochaib/chaiwiki/wiki/VPS%E5%BC%80%E6%94%BE%E7%AB%AF%E5%8F%A3%E5%B8%B8%E8%A7%84%E6%96%B9%E6%B3%95%EF%BC%81)
<br />感谢github emptysuns大佬开发如此好用的一键脚本，适配ubuntu/debian, centos/rhel操作系统,misple/arm/x86/s390x架构
<pre><code>bash <(curl -fsSL https://git.io/hysteria.sh)</pre></code>

### 4、json客户端配置文件下载、快捷导入保存
按下图操作，在Finalshell中找到文件，点击右边刷新，然后找到json结尾的文件下载即可；<br />
同时，把图中绿色部分hysteria:开头的这一行复制下来，保存到一个文本中，后续会用到
<img width="1016" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/42cd1dbb-3be2-4759-9f74-b0aedf39fbc8">


# 管理面板
安装完成后，输入 hihy 就能看到管理面板，如下图片所示，可以重新查看面板信息，按功能输入对应数字即可操作；<br />
如果想重新配置Hysteria，输入数字9运行，即可重新更改配置
<img width="1016" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/34f667da-3ede-4f6f-8c77-d00a90f53659">
如果要重新查看Hysteria配置，输入hihy后，输入8，就可以重新查看配置
<img width="1016" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/cfbd4c2d-f8ea-4519-a4bb-be199a0cec95">


# 二维码生成
可以使用下面的二维码生成，将前面生成的快捷链接生成二维码，让客户端扫码导入配置文件实现科学上网<br />
https://cli.im/

# 常见问题排查、说明
脚本作者有针对使用过程中出现的问题有说明和解释，如果遇到问题，可查看官方开源界面的补充或更新<br />
脚本开源界面：https://github.com/emptysuns/hysteria<br />
问题说明界面：https://github.com/emptysuns/Hi_Hysteria/blob/main/md/issues.md

# Hysteria客户端下载
Hysteria各平台客户端推荐列表，请访问：https://github.com/emptysuns/Hi_Hysteria/blob/main/md/client.md<br />
Windows需要使用和内核一起打包的V2RayN客户端，下载链接如下：<br />
**Windows：**[v2rayN下载](https://github.com/emptysuns/Hi_Hysteria/releases)<br />
<img width="827" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/5cd1fffb-ada9-46a3-ab3b-60f003fda1e9">


**苹果IOS、iPad**：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜，并支持Hysteria）<br />
不管是iPad平板还是iPhone手机，比较推荐的科学上网软件必定是：Shadowrocket，但是需要注册一个非国区或美区账号才能进行购买，目前是2.99美刀约20块人民币，注册美区账号和充值购买也非常简单，请参考以下两篇文章。<br />
如何注册美区Apple ID:https://zhuanlan.zhihu.com/p/635054054<br />
美区账号如何充值：https://zhuanlan.zhihu.com/p/636121931<br />
注册美区ID并按以上方法充值后，在App Store中搜索Shadowrocket购买并下载安装<br />

**安卓：**[NekoBox](https://github.com/MatsuriDayo/NekoBoxForAndroid/releases) 注意，下方的Hysteria 插件也要一并下载并安装，视频中漏说了<br /><br />
<img width="882" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/f1db56a8-7105-4a26-9784-0089842451b4">
安卓还要下载这个插件：[Hysteria 插件](https://github.com/MatsuriDayo/plugins/releases)
<img width="1101" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/333f3c18-6f44-4495-af94-9a38d3a606fd">
安卓手机，将NekoBox和Hysteria plugins两个都下载，导入到安卓手机，都安装即可，NekoBox正常运行需要依赖Hysteria plugins


**OpenWRT软路由：**[参考这个链接](https://github.com/emptysuns/Hi_Hysteria/blob/main/md/client.md#4-openwrt-passwall
)<br /><br />


# 结尾
本次一键脚本开源界面：https://github.com/emptysuns/Hi_Hysteria<br />
一**郑重声明：请合理使用科学上网于学习知识、外贸或科研工作方面，遵守相关规定**<br />

