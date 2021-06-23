# Welcome to RoutePoison.com

&nbsp;<a href="https://github.com/routepoison"><img src="https://badgen.net/badge/github/routepoison/green?icon=github"></a><a href="https://routepoison.com"><img src="https://badgen.net/badge/personal-website/routepoison/green"></a><a href="https://routepoison.com"><img src="https://badgen.net/badge/academic-website/routepoison/green"></a><a href="https://routepoison.com"><img src="https://badgen.net/badge/professional-website/routepoison/green"></a>&nbsp;

This is my personal website and an open sourced I.T. training repository.

🔗 [Join the Discord!](https://discord.gg/GN4tyGZtfP)

<img src="./img/discord-logo-1024x1024.png" height="150" width="150">

## 🗄 Directory

* 📁 [Networking](./#)
    + 📁 [Data Center](./#)
        - 📋 [vPC Technology Configuration](./networking/data-center/NX-OS_vPC.md) 
    + 📁 [DMVPN](./#)
        - 📋 [DMVPN Phase I](./networking/dmvpn/phase1.md)
    + 📁 [Routing](./#)
        - 📄 [Administrative Distance](./networking/routing/admin-distances.md)
        - 📄 [RFC1918 Prefix-List](./networking/routing/prefix-list.md)
        - 📄 [Subnet Mask Table](./index.md#subnetwildcard-mask-table)
        - 📄 [VRF](./networking/routing/vrf.html)
    + 📁 [Security](./#)
        - 📋 [Cisco ASA Failover Configuration](./networking/firewall/asa-failover.md)
        - 📋 [Cisco ASA Packet-Tracer & Captures](./networking/firewall/asa-packet-tracer_capture.md)
        - 📋 [Cisco ASA Transparent Mode](./networking/firewall/asa-transparent-mode.md)
    + 📁 [Switching](./#)
    + 📁 [TCP/IP](./#)

## 📓 Certification Testing

* 📁 [Antiquated Exams](./#)
    + 📁 [Antiquated Exams](./archive/README.md)
        - 📜 [BSCI 642-901](./archive/antiquated-exams/BSCI642-901/BSCI_CCNP-642-901.md)
    + 📁 [Cisco Training](./#)
        -  📁 [Cisco CCNA](./certifications/README.md)
        -  📁 [Cisco CCNP](./certifications/README.md)
        -  📁 [Cisco CCIE](./certifications/README.md)

## 🌎 Internet

* [BGP Stream](http://bgpstream.com/)
* [BGP Advanced Internet Resources](https://www.bgp4.as/)
* [RFC Archive](https://www.rfc-archive.org/)

## Programming

* 📁 [Cryptocurrency](./#)
* 📁 [Hacking](./#)
    + 🔴 [Redteam](./hacking/redteam/kali-network-cookbook.html)
        - 🧮 [Portscanning](./hacking/redteam/kali-network-cookbook/portscan.html)
    + 🔵 [Blueteam](./hacking/blueteam/#)

* 📁 [Programming](./programming/)
    + 📁 [C++](./programming/cpp/cpp-crash-course/toc.md)

## 🛠 Resources

*

---

## Calendar Updates

### 📆 June 4th

Alrighty then, it's been a while - I get a bit busy with work and what not (who doesn't). However! I do have some new content and I've been grinding hard so I'm just about ready to start advertising my content.


### 📆 June 4th

Start programming section amongst other updates.

### 📆 May 7th

Restructuring in progress

### 📆 April 28th

Quick and dirty router configuration to filter RFC1918 IP address space:

```
ip prefix-list RFC1918 seq 5 permit 192.168.0.0/12 ge 32
ip prefix-list RFC1918 seq 10 deny 0.0.0.0/0 ge 32
ip prefix-list RFC1918 seq 15 permit 10.0.0.0/7 ge 8
ip prefix-list RFC1918 seq 20 permit 172.16.0.0/11 ge 12
ip prefix-list RFC1918 seq 25 permit 192.168.0.0/15 ge 16
```

This is [archived here](./networking/routing/prefix-list.md).

### 📆 April 10th

#### 🔗 RFC1918, Subnets, and Wildcard Masks

| RFC1918 | IP Address Range | Number of Addresses | Classful Description | Largest CIRD Block | Host ID Size|
|:-:|:-:|:-:|:-:|:-:|:-:|
| 24-bit block | 10.0.0.0 - 10.255.255.255 | 16,777,216 | Single Class A | 10.0.0.0/8 (255.0.0.0) | 25 bits |
| 20-bit block | 172.16.0.0 - 172.31.255.255 | 1,048,576 | 16 Contiguous Class Bs | 172.16.0.0/12 (255.240.0.0) | 20 bits|
| 16-bit block | 192.168.0.0 - 192.168.255.255 | 65,536 | 256 contiguous class Cs | 192.168.0.0/16 (255.255.0.0) | 16 bits |

#### 🔗 Subnet/Wildcard Mask Table

| /Slash | Number of Hosts | Subnet Mask/Netmask | Wildcard Mask |
|:-:|:-:|:-:|:-:|
|/30|4|255.255.255.252|0.0.0.3|
|/29|8|255.255.255.248|0.0.0.7|
|/28|16|255.255.255.240|0.0.0.15|
|/27|32|255.255.255.224|0.0.0.31|
|/26|64|255.255.255.192|0.0.0.63|
|/25|128|255.255.255.128|0.0.0.127|
|/24|256|255.255.255.0|0.0.0.255|
|/23|512|255.255.254.0|0.0.1.255|
|/22|1024|255.255.252.0|0.0.3.255|
|/21|2048|255.255.248.0|0.0.7.255|
|/20|4096|255.255.240.0|0.0.15.255|
|/19|8192|255.255.224.0|0.0.31.255|
|/18|16384|255.255.192.0|0.0.63.255|
|/17|32768|255.255.128.0|0.0.127.255|
|/16|65536|255.255.0.0|0.0.255.255|
|/15|131072|255.255.0.0|0.1.255.255|
|/14|262144|255.254.0.0|0.3.255.255|
|/13|524288|255.242.0.0|0.7.255.255|
|/12|1048576|255.240.0.0|0.15.255.255|
|/11|2097152|255.224.0.0|0.31.255.255|
|/10|4194304|255.192.0.0|0.63.255.255|
|/9|8388608|255.128.0.0|0.127.255.255|
|/8|16777216|255.0.0.0|0.255.255.255|

---

### 📆 April 10th

#### 🔗 IPSec Authentication Header Format

```
    0                   1                   2                   3
    0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
   | Next Header   |  Payload Len  |          RESERVED             |
   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
   |                 Security Parameters Index (SPI)               |
   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
   |                    Sequence Number Field                      |
   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
   |                                                               |
   +                Authentication Data (variable)                 |
   |                                                               |
   +-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
```

---

### 📆 April 8th

Site is now off Google, up, and operational!

![Bubbles](./img/bubbles.gif)

---

## 🔗 Emoji Legend

| Emoji | Definition/Purpose |
|:-:|:-:|
|🔥|Firewall|📆|Daily Entry|
|🔖|Lesson Topic|📰|Daily Entry 2|
|📃|Lesson Subtopic|📅|Daily Entry 3|
|📄|Publication|📁|Website Directory|
|📜|Script|📂|Current Website Directory| 
|↩️|Return back a page|🟢| Available|
|✉️|E-Mail|🟡|Under Maintenance|
|🔗| URL|🔴|Unavailable|

---

Thanks for stopping by visitor #: <script type="text/javascript" src="//counter.websiteout.net/js/5/0/1000/0"></script>

🔧: [Github @routepoison](https://github.com/routepoison)<br>
📸: [Instagram: @theproxyrunner](https://www.instagram.com/theproxyrunner/)<br>
🐦: [Twitter: @proxy_runner](https://twitter.com/proxy_runner)<br>
✉️ <a href="mailto:gs@routepoison.com">Send me an email</a><br>
