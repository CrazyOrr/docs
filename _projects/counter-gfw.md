---
layout: default
name: 科学上网
---
# 科学上网
![防火长城](https://upload-images.jianshu.io/upload_images/5979866-02263a38e7041b95.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/348)

## 1 什么是“科学上网”
GFW(Great Firewall)，防火长城，在中国大陆屏蔽了[Google](https://google.com/)、[Wikipedia](https://www.wikipedia.org/)等一系列国际网站。

“你有张良计，我有过墙梯”。从[goagent](https://github.com/goagent/goagent/)到[shadowsocks](https://github.com/shadowsocks/shadowsocks)，再到[v2ray](https://github.com/v2ray/v2ray-core)。
使用这一代一代的技术“翻墙”上外网，就是所谓的“科学上网”。目前我使用的“科学上网”方式主要是海外VPS配合shadowsocks或者v2ray。

## 2 什么是VPS
VPS(Virtual Private Server)，虚拟专用服务器，原本主要是建站使用的。在天朝GFW的特殊网络环境下，“曲线救国”，大量用来安装shadowsocks或者v2ray作为代理服务器“翻墙”。
下面介绍我使用过的BandwagonHost和Vultr。

### 2.1 BandwagonHost
由于发音类似，俗称“搬瓦工”。隶属于加拿大 IT7 Networks 旗下，从 2004 年开始开始提供虚拟主机、VPS、独立服务器等服务。
付费方案从最初的 $3.99、$4.99 年付，慢慢升级到 $19.99 年付，再到现在的 $49.99 年付，质量也越来越好。
目前已经支持支付宝、微信支付等支付方式，购买使用非常方便。

#### 2.1.1 机房选择
目前搬瓦工的机房推荐顺序如下（按照推荐的优先级排序，最前面的是最推荐的）：

1. 中国香港 HONG KONG CN2 GIA：质量最佳，价格较高（$1599.99/年起），土豪不差钱用户以及高端用户首选。
2. 美国洛杉矶 DC6 CN2 GIA ECOMMERCE：中美最快线路，性价比最高（$169.99/年起，更有限量方案 $49.99/年），中高端选择，目前推荐。
3. 美国洛杉矶 DC9 CN2 GIA：中美最快线路，线路质量和 DC6 不相上下，但是目前起步门槛较高（$339.99/年起），中高端选择。
4. 美国洛杉矶 DC8 CN2：中美直连，比 CN2 GIA 线路等级低，但是大部分地区表现良好，入门之选，目前最便宜的方案（$49.99/年）。
5. 美国洛杉矶 DC3 CN2：中美直连，比 DC8 CN2 质量稍差，备选线路。
6. 美国洛杉矶 MCOM、QNET 等其他机房：这几个机房在所有方案里都可以选择，一般我们不是特殊用途不会考虑。

#### 2.1.2 付费方案选择
付费方案和上面的机房是对应的，比如：

- 中国香港 HONG KONG CN2 GIA 方案：仅可使用香港 HONG KONG CN2 GIA 机房；
- 美国洛杉矶 CN2 GIA ECOMMERCE 方案：可以使用 DC6 CN2 GIA ECOMMERCE、DC9 CN2 GIA、DC8 CN2、DC3 CN2 等机房。
- 美国洛杉矶 CN2 GIA 方案：可以使用 DC9 CN2 GIA、DC8 CN2、DC3 CN2 等机房。
- 美国洛杉矶 CN2 方案：可以使用 DC8 CN2、DC3 CN2 等机房。

高端方案包含低端方案的机房，越高端选择面越广。

| 方案 | 内存 | CPU | 硬盘 | 流量/月 | 带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| CN2 | 1GB | 1核 | 20GB | 1TB | 1Gbps | $49.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=57) |
| CN2 | 2GB | 1核 | 40GB | 2TB | 1Gbps | $52.99/半年<br>$99.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=58) |
| CN2 | 4GB | 2核 | 80GB | 3TB | 1Gbps | $59.99/季度<br>$199.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=59) |
| CN2 | 8GB | 2核 | 160GB | 5TB | 1Gbps | $39.99/月<br>$399.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=67) |
| CN2 | 16GB | 3核 | 320GB | 8TB | 1Gbps | $79.99/月<br>$799.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=68) |
| CN2 GIA | 1GB | 2核 | 20GB | 1TB | 1Gbps | $31.99/季度<br>$113.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=72) |
| CN2 GIA | 2GB | 3核 | 40GB | 2TB | 1Gbps | $61.99/季度<br>$225.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=73) |
| CN2 GIA | 4GB | 4核 | 80GB | 3TB | 1Gbps | $39.99/月<br>$399.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=74) |
| CN2 GIA | 8GB | 6核 | 160GB | 5TB | 1Gbps | $75.99/月<br>$759.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=75) |
| CN2 GIA | 16GB | 8核 | 320GB | 8TB | 1Gbps | $143.99/月<br>$1439.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=76) |
| CN2 GIA ECOMMERCE | 1GB | 2核 | 20GB | 1TB | 2.5Gbps | $49.99/季度<br>$169.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=87) |
| CN2 GIA ECOMMERCE | 2GB | 3核 | 40GB | 2TB | 2.5Gbps | $89.99/季度<br>$299.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=88) |
| CN2 GIA ECOMMERCE | 4GB | 4核 | 80GB | 3TB | 2.5Gbps | $56.99/月<br>$549.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=89) |
| CN2 GIA ECOMMERCE | 8GB | 6核 | 160GB | 5TB | 5Gbps | $86.99/月<br>$879.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=90) |
| CN2 GIA ECOMMERCE | 16GB | 8核 | 320GB | 8TB | 5Gbps | $159.99/月<br>$1599.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=91) |
| CN2 GIA ECOMMERCE | 32GB | 10核 | 640GB | 10TB | 10Gbps | $289.99/月<br>$2759.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=92) |
| CN2 GIA ECOMMERCE | 64GB | 12核 | 1280GB | 12TB | 10Gbps | $549.99/月<br>$5399.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=93) |
| HONG KONG CN2 GIA | 2GB | 2核 | 40GB | 0.5TB | 1Gbps | $89.99/月<br>$899.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=95) |
| HONG KONG CN2 GIA | 4GB | 4核 | 80GB | 1TB | 1Gbps | $155.99/月<br>$1559.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=96) |
| HONG KONG CN2 GIA | 8GB | 6核 | 160GB | 2TB | 1Gbps | $299.99/月<br>$2999.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=97) |
| HONG KONG CN2 GIA | 16GB | 8核 | 320GB | 4TB | 1Gbps | $589.99/月<br>$5899.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=98) |
| KVM | 1GB | 2核 | 20GB | 1TB | 1Gbps | $49.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=44) |
| KVM | 2GB | 3核 | 40GB | 2TB | 1Gbps | $52.99/半年<br>$99.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=45) |
| KVM | 4GB | 4核 | 80GB | 3TB | 1Gbps | $19.99/月<br>$199.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=46) |
| KVM | 8GB | 5核 | 160GB | 4TB | 1Gbps | $39.99/月<br>$399.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=47) |
| KVM | 16GB | 6核 | 320GB | 5TB | 1Gbps | $79.99/月<br>$799.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=48) |
| KVM | 24GB | 7核 | 480GB | 6TB | 1Gbps | $119.99/月<br>$1199.99/年 | [购买](https://bwh88.net/aff.php?aff=61530&pid=49) |

#### 2.1.3 最新优惠券
- 2020-01-13 BWH3HYATVBJW（优惠力度 6.58%）

### 2.2 [Vultr](https://www.vultr.com/?ref=8660127-6G)
[**注册即送100美元活动**](https://www.vultr.com/?ref=8660127-6G)

| 硬盘 | CPU | 内存 | 流量/月 | 价格 |
| --- | --- | --- | --- | --- |
| 10GB | 1核 | 512MB | 0.5TB | $3.5/月 |
| 25GB | 1核 | 1024MB | 1TB | $5/月 |
| 55GB | 1核 | 2GB | 2TB | $10/月 |
| 80GB | 2核 | 4GB | 3TB | $20/月 |
| 160GB | 4核 | 8GB | 4TB | $40/月 |
| 320GB | 6核 | 16GB | 5TB | $80/月 |
| 640GB | 8核 | 32GB | 6TB | $160/月 |
| 1280GB | 16核 | 64GB | 10TB | $320/月 |
| 1600GB | 24核 | 96GB | 15TB | $640/月 |

## 3 翻墙软件
### 3.1 shadowsocks
- [shadowsocks](https://hijk.art/shadowsocks-ss-one-click-script/)
- [shadowsocksr](https://hijk.art/shadowsocksr-ssr-one-click-script/)

### 3.2 v2ray
- [教程](https://tlanyan.me/v2ray-tutorial/)
- [客户端](https://tlanyan.me/v2ray-clients-download/)
