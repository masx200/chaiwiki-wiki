# 前言



# 首先，你需要一个VPS服务器
待定
如果真的不想自建，想用机场，那么我推荐你使用搬瓦工官方JMS机场，非常稳定、不跑路！<br />
[搬瓦工JMS机场使用图文指引！点我~](https://github.com/bigtouchai/chaiwiki/wiki/%E6%9C%80%E7%A8%B3%E6%9C%BA%E5%9C%BA%EF%BC%9A%E6%90%AC%E7%93%A6%E5%B7%A5Just-My-Socks-%E6%9C%BA%E5%9C%BA%E5%A6%82%E4%BD%95%E8%B4%AD%E4%B9%B0%E4%BD%BF%E7%94%A8%E3%80%81%E5%A6%82%E4%BD%95%E9%85%8D%E7%BD%AE%E5%AE%A2%E6%88%B7%E7%AB%AF)

# 域名购买
可使用Goday：[官网](https://www.godaddy.com/)或namesilo等域名注册商购买域名，推荐使用namesilo，免费的whois隐私保护！<br />
NameSilo官网：[namesilo官网](https://www.namesilo.com/)

# SSH连接工具（任选一个）
FinalShell(推荐):[FinalShell下载](http://www.hostbuf.com/t/988.html)<br />
MobaXterm:[MobaXterm官网](https://mobaxterm.mobatek.net/)

# 正式安装、搭建节点

### 1、必要更新操作(Debian/Ubuntu)
<pre><code>apt update -y</pre></code>
<pre><code>apt install -y curl socat</pre></code>
**注意：**如果是centos系统，则分别运行yum update -y和yum install -y curl socat


### 2、安装x-ui
感谢github vaxilu大佬开发如此好用的一键脚本
<pre><code>bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)</pre></code>

### 3、证书申请（开TLS提升安全性必备）
<pre><code>curl https://get.acme.sh | sh</pre></code>
<pre><code>~/.acme.sh/acme.sh --register-account -m 你的邮箱</pre></code>

<pre><code>~/.acme.sh/acme.sh --issue -d 你的域名 --standalone</pre></code>
更改证书存放位置
<pre><code>~/.acme.sh/acme.sh --installcert -d 你的域名 --key-file /root/private.key --fullchain-file /root/cert.crt</pre></code>


# 全平台客户端下载
[V2Ray官网对于全平台客户端的总结和一览](https://www.v2ray.com/awesome/tools.html)<br />

Windows：[v2rayN下载](https://github.com/2dust/v2rayN/releases)<br />
IOS：App Store中，登录非国区账号，安装Shadowrocket小火箭（推荐，协议支持全面、便宜）<br />
安卓：[V2RayNG](https://github.com/2dust/v2rayNG/releases)<br />
苹果MAC OS：[V2RayU下载](https://github.com/yanue/V2rayU/releases)<br />
