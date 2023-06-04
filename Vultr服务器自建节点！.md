### Vultr服务器购买
自建节点需要有一台VPS服务器，本次推荐Vultr家的VPS服务器，[Vultr官网](https://www.vultr.com/?ref=9467366)，2014年成立，性价比高，可随时免费更换IP、不用担心IP不够用，机器、网络运行稳定性佳，并且提供超过32个机房可选。<br />
![1685845552674](https://github.com/xiaochaib/chaiwiki/assets/134616948/9306a881-8aa8-4970-a7d4-3ce32fbe6e93)


如果追求极致速度，可考虑使用搬瓦工VPS。[搬瓦工VPS官网](https://bwh88.net/aff.php?aff=71506)，以下是推荐用来自建节点的机房，可点链接直达。<table role="table">
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



### Vultr开放端口
Vultr目前机器只默认开放SSH端口22，其它一些端口全部需要手动开放。
<pre><code>apt-get install firewalld -y</pre></code>
443处替换成你需要开放的端口号
<pre><code>firewall-cmd --zone=public --add-port=443/tcp --permanent</pre></code>
每次新开放端口后，重启防火墙
<pre><code>firewall-cmd --reload</pre></code>
