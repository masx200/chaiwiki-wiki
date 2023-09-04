### VPS服务器购买
自建节点需要有一台VPS服务器，如想月付，可使用Vultr家的VPS服务器，[Vultr官网](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，目前月付5刀/月，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过几十个机房可选，支持支付宝。<br />

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

### Vultr注册、充值、部署机器
新用户，请点击上方蓝色字体，鼠标右键-新标签中打开，进入Vultr官网进入注册
<img width="1118" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/02508f07-2659-46e0-98b8-1875705a9f30">
进入官网后，可以用浏览器翻译，或者按下方提示，输入邮箱、密码注册账号，注册完成后，点击右上角头像-Log in登录
<img width="1438" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/807cd43a-a933-4d50-8ddf-cb041b447ece">
登录后，点击Account-Make a payment，选择Alipay（支付宝），最低充值10美金（约60多块），按提示扫码充值；成功后，右上角会显示余额
<img width="1438" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/5113b485-d18c-4524-8e27-4c4965f2d601">
充值后就可以进行服务器部署，点击Product-Computer-Deploy New Server进行部署VPS界面
<img width="1439" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/d5c0a087-a6f6-463d-b415-9145a6679db2">
推荐常规5美金/月的机器，按下图选择：Cloud Compute-Regular Performance
<img width="1433" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/648de14e-a2ae-4439-92bf-f9374d5287ef">
然后往下拉，选择要把机器部署在哪个国家，一般来说美国地区的速度好，可选美国
<img width="1154" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/36fbbeee-86de-4ee0-91bd-c27c303e20a8">

往下拉，选择安装什么系统，如果是用来上网，推荐Ubutu 20.04及以上版本系统，对各种脚本兼容性好
<img width="1143" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/ec732b86-57bc-48d5-a3b8-7442ae7109d0">
按情况选择套餐，入门是5美金/月，每个月1T流量，足够用了
<img width="1207" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/d29dc3a0-d8a3-4b22-a9f5-21abe1868fbf">
往下拉，关闭自动备份；按需设置是否要开启IPV6
<img width="1241" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/0a15059b-0e4c-4d9f-bf6a-ba1361c8de73">
确认价格，正确后点击Deploy Now部署
<img width="1226" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/fb920418-84f6-46d5-b533-280b491ab1ab">

部署完成后，点击Product-Computer就可看到成功部署的服务器
<img width="1018" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/02570cb6-44f3-416e-920c-b3c4266f046e">



### 检测服务器状态
Vultr VPS服务器开通后，有机率会分配到被墙的IP，但胜在Vultr是按时计费的，所以可以随时销毁机器进行新IP分配（新建的机器要5分钟后才能执行销毁）。<br />
<img width="1440" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/7b6c49ce-d23d-4b6f-8940-0bd9889c1109">


机器开通后大概3-5分钟（一定要3-5分钟后再检测，刚新建的机器初始化中），复制机器的IP到以下网址进行ping检测，如可以检测通过就代表这个IP可用，否则，销毁机器，按前面新建机器的步骤重新来一次，再检测IP，直到IP可用。
PING工具：[ping工具（检测服务器IP是否可用）](https://ping.chinaz.com/)
<img width="1440" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/a090dee6-75f7-445a-a275-b016610fbf38">

### # VPS登录信息获取
部署开机后，可以按以下操作获取VPS的IP、root密码等等，Vultr默认SSH端口是22
<img width="1440" alt="image" src="https://github.com/xiaochaib/chaiwiki/assets/134616948/f24e2b8f-d98b-4ac4-bb3e-f190b81c5b68">



### # SSH连接工具
任选其中一个即可<br />
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)


### 手动开放端口
Vultr目前机器只默认开放SSH端口22，其它一些端口全部需要手动开放，依次复制以下命令运行就行!注意，以下操作仅适用于Ubuntu 20.04版本系统，请在Vultr部署时选择这个版本系统<br />
首先，需要安装防火墙，复制以下命令到ssh中运行就行
<pre><code>apt-get install firewalld -y && firewall-cmd --zone=public --add-port=22/tcp --permanent && firewall-cmd --reload</pre></code>

根据你获取的节点信息，记下节点信息中的端口（port）号，将记下的端口号替换到下方命令中的『端口』两字中，即是完整命令，运行即可、当然，x-ui面板的端口首先要开放
<pre><code>firewall-cmd --zone=public --add-port=端口/tcp --permanent && firewall-cmd --reload</pre></code>
注意，后续如果重新配置节点信息，端口有变动，切记重新运行以上放行端口的命令，不然会导致节点无法使用，切记

参考Vultr官方文档对于放行端口的说明：https://www.vultr.com/docs/firewall-quickstart-for-vultr-cloud-servers/


# 结尾
一请合理使用科学上网，遵守当地法律法规<br />

