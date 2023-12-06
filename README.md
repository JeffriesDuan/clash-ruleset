# 一、 说明
## 1. rule-set 规则
① 规则参考 [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules)，有如下分类：
```
  - RULE-SET,ads,🛑 广告拦截
  - RULE-SET,private,🔒 私有网络
  - RULE-SET,microsoft-cn,Ⓜ️ 微软服务
  - RULE-SET,apple-cn,🍎 苹果服务
  - RULE-SET,google-cn,📢 谷歌服务
  - RULE-SET,games-cn,🎮 游戏平台
  - RULE-SET,netflix,🎥 奈飞视频
  - RULE-SET,disney,📽️ 迪士尼+
  - RULE-SET,max,🎞️ Max
  - RULE-SET,primevideo,🎬 Prime Video
  - RULE-SET,appletv,🍎 Apple TV+
  - RULE-SET,youtube,📹 油管视频
  - RULE-SET,tiktok,🎵 TikTok
  - RULE-SET,bilibili,📺 哔哩哔哩
  - RULE-SET,ai,🤖 人工智能
  - RULE-SET,networktest,📈 网络测试
  - RULE-SET,applications,🖥️ 直连软件
  - RULE-SET,proxy,🪜 代理域名
  - RULE-SET,cn,🔗 直连域名
  - RULE-SET,telegramip,📲 电报消息
  - RULE-SET,privateip,🔒 私有网络
  - RULE-SET,cnip,🇨🇳 国内 IP
```
② 每天早上 3 点（北京时间）自动构建生成  
③ `RULE-SET:ads` 源采用 [privacy-protection-tools/anti-AD/anti-ad-clash.yaml](https://github.com/privacy-protection-tools/anti-AD)   
④ `RULE-SET:private` 源采用 [v2fly/domain-list-community/private](https://github.com/v2fly/domain-list-community/blob/master/data/private) 和 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan) 组合，并添加主流 Clash dashboard 在线面板域名（`clash.razord.top`、`clash.metacubex.one`、`yacd.haishan.me`、`yacd.metacubex.one` 和 `d.metacubex.one`）  
⑤ `RULE-SET:microsoft-cn` 源采用 [v2fly/domain-list-community/microsoft@cn](https://github.com/v2fly/domain-list-community/blob/master/data/microsoft)  
⑥ `RULE-SET:apple-cn` 源采用 [felixonmars/dnsmasq-china-list/apple.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑦ `RULE-SET:google-cn` 源采用 [felixonmars/dnsmasq-china-list/google.china.conf](https://github.com/felixonmars/dnsmasq-china-list)  
⑧ `RULE-SET:games-cn` 源采用 [v2fly/domain-list-community/category-games@cn](https://github.com/v2fly/domain-list-community/blob/master/data/category-games)、[blackmatrix7/ios_rule_script/SteamCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/SteamCN) 和 [blackmatrix7/ios_rule_script/GameDownloadCN](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Game/GameDownloadCN) 组合  
⑨ `RULE-SET:netflix` 源采用 [blackmatrix7/ios_rule_script/Netflix/Netflix_Classical.yaml](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Netflix)  
⑩ `RULE-SET:disney` 源采用 [blackmatrix7/ios_rule_script/Disney](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Disney)  
⑪ `RULE-SET:max` 源采用 [blackmatrix7/ios_rule_script/HBO](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/HBO)  
⑫ `RULE-SET:primevideo` 源采用 [blackmatrix7/ios_rule_script/PrimeVideo](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/PrimeVideo)  
⑬ `RULE-SET:appletv` 源采用 [blackmatrix7/ios_rule_script/AppleTV](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/AppleTV)  
⑭ `RULE-SET:youtube` 源采用 [blackmatrix7/ios_rule_script/YouTube](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/YouTube)  
⑮ `RULE-SET:tiktok` 源采用 [blackmatrix7/ios_rule_script/TikTok](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/TikTok)  
⑯ `RULE-SET:bilibili` 源采用 [blackmatrix7/ios_rule_script/BiliBili](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BiliBili)  
⑰ `RULE-SET:ai` 源采用 [blackmatrix7/ios_rule_script/OpenAI/OpenAI.yaml](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/OpenAI)、[blackmatrix7/ios_rule_script/Bing/Bing.yaml](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Bing) 和 [blackmatrix7/ios_rule_script/BardAI/BardAI.yaml](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/BardAI) 组合  
⑱ `RULE-SET:networktest` 源采用 [blackmatrix7/ios_rule_script/Speedtest](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Speedtest) 和 IPv6 测试网站（采用 `keyword` 关键字）组合  
⑲ `RULE-SET:applications` 源采用 [Loyalsoldier/clash-rules/applications.txt](https://github.com/Loyalsoldier/clash-rules/tree/release)  
⑳ `RULE-SET:proxy` 源采用 [cokebar/gfwlist2dnsmasq](https://github.com/cokebar/gfwlist2dnsmasq) 生成的 [gfwlist](https://github.com/gfwlist/gfwlist) 和 [Loyalsoldier/domain-list-custom/geolocation-!cn.txt](https://github.com/Loyalsoldier/domain-list-custom) 组合  
㉑ `RULE-SET:cn` 源采用 [blackmatrix7/ios_rule_script/ChinaMax/ChinaMax_Domain.yaml](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaMax)  
㉒ `RULE-SET:telegramip` 源采用 [Telegram IP](https://core.telegram.org/resources/cidr.txt)  
㉓ `RULE-SET:privateip` 源采用 [blackmatrix7/ios_rule_script/Lan](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Lan)（IP 部分）  
㉔ `RULE-SET,cnip` 取自 [DustinWin/clash-geoip](https://github.com/DustinWin/clash-geoip)，源采用 [GeoLite2/cn.txt](https://dev.maxmind.com/geoip/geolite2-free-geolocation-data)、[17mon/china_ip_list](https://github.com/17mon/china_ip_list)、[gaoyifan/china-operator-ip](https://github.com/gaoyifan/china-operator-ip) 和 [blackmatrix7/ios_rule_script/ChinaIPs/ChinaIPs_IP.txt](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/ChinaIPs) 组合
## 2. user.yaml  
① 添加[常用 fake-ip 地址过滤列表](https://github.com/juewuy/ShellClash/blob/master/public/fake_ip_filter.list)到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，提高兼容性  
② 添加 [TrackersList](https://trackerslist.com)（udp 域名）到 fake-ip-user.yaml 内的 `fake-ip-filter` 中，防止 [BT 下载](https://github.com/c0re100/qBittorrent-Enhanced-Edition/releases)无法连接 TrackersList UDP 协议  
<img src="https://user-images.githubusercontent.com/45238096/224113233-4d76dec2-495c-4790-a00e-538fc1469639.png" width="60%"/>  
③ 添加如下域名，以配合 AdGuardHome 作为下游时解决下载“DNS 黑名单”失败的问题：
```
    - 'adguardteam.github.io'
    - 'anti-ad.net'
```
④ 若想自己生成配置文件 user.yaml，可以 [Fork 本项目](https://github.com/DustinWin/clash-ruleset/fork)后编辑 *.github/workflows/rule-set.yml* 文件内的 `name: Generate xxx-user.yaml` 部分  
⑤ 若 DNS 模式选用的是 `redir-host`，需要进行 DNS 分流（可以参考《[ShellClash 使用 Clash.Meta 内核进行 DNS 分流教程-ruleset 方案](https://github.com/DustinWin/clash-tutorials/blob/main/%E6%95%99%E7%A8%8B%E5%90%88%E9%9B%86/%E8%BF%9B%E9%98%B6%E7%AF%87/ShellClash%20%E4%BD%BF%E7%94%A8%20Clash.Meta%20%E5%86%85%E6%A0%B8%E8%BF%9B%E8%A1%8C%20DNS%20%E5%88%86%E6%B5%81%E6%95%99%E7%A8%8B-ruleset%20%E6%96%B9%E6%A1%88.md)》），可以进入 *.github/workflows/rule-set.yml* 文件，编辑 `Generate redir-host-user.yaml` 部分，将 `nameserver` 中的 `🪜 代理域名`改成可以访问外网的策略组名称，或者直接将 `'https://dns.google/dns-query#🪜 代理域名'` 修改为 `'tls://dns.google'`
# 二、 使用方法
在配置文件中新增如下内容：
- 注：以下只是节选，请酌情套用

```
proxy-groups:
  - {name: 📈 网络测试, type: select, proxies: [🎯 全球直连, 🇭🇰 香港节点, 🇹🇼 台湾节点, 🇯🇵 日本节点, 🇰🇷 韩国节点, 🇸🇬 新加坡节点, 🇺🇸 美国节点]}

  - {name: 🔗 直连域名, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}

  - {name: 🪜 代理域名, type: select, proxies: [🚀 节点选择, 🎯 全球直连]}

  - {name: 🎮 游戏平台, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}

  - {name: 🎥 奈飞视频, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 📽️ 迪士尼+, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 🎞️ Max, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 🎬 Prime Video, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 🍎 Apple TV+, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 📹 油管视频, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 🎵 TikTok, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 📺 哔哩哔哩, type: select, proxies: [🎯 全球直连, 🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点]}

  - {name: 🤖 人工智能, type: select, proxies: [🚀 节点选择, 🇭🇰 香港节点, 🇯🇵 日本节点, 🇸🇬 新加坡节点, 🇺🇸 美国节点]}

  - {name: Ⓜ️ 微软服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}

  - {name: 📢 谷歌服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}

  - {name: 🍎 苹果服务, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}

  - {name: 🇨🇳 国内 IP, type: select, proxies: [🎯 全球直连, 🚀 节点选择]}

  - {name: 📲 电报消息, type: select, proxies: [🚀 节点选择]}

  - {name: 🖥️ 直连软件, type: select, proxies: [🎯 全球直连]}

  - {name: 🔒 私有网络, type: select, proxies: [🎯 全球直连]}

  - {name: 🛑 广告拦截, type: select, proxies: [REJECT]}

  - {name: 🎯 全球直连, type: select, proxies: [DIRECT]}

rule-providers:
  ads:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/ads.yaml"
    path: ./ruleset/ads.yaml
    interval: 86400

  private:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/private.yaml"
    path: ./ruleset/private.yaml
    interval: 86400

  microsoft-cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/microsoft-cn.yaml"
    path: ./ruleset/microsoft-cn.yaml
    interval: 86400

  apple-cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/apple-cn.yaml"
    path: ./ruleset/apple-cn.yaml
    interval: 86400

  google-cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/google-cn.yaml"
    path: ./ruleset/google-cn.yaml
    interval: 86400

  games-cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/games-cn.yaml"
    path: ./ruleset/games-cn.yaml
    interval: 86400

  netflix:
    type: http
    behavior: classical
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/netflix.yaml"
    path: ./ruleset/netflix.yaml
    interval: 86400

  disney:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/disney.yaml"
    path: ./ruleset/disney.yaml
    interval: 86400

  max:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/max.yaml"
    path: ./ruleset/max.yaml
    interval: 86400

  primevideo:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/primevideo.yaml"
    path: ./ruleset/primevideo.yaml
    interval: 86400

  appletv:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/appletv.yaml"
    path: ./ruleset/appletv.yaml
    interval: 86400

  youtube:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/youtube.yaml"
    path: ./ruleset/youtube.yaml
    interval: 86400

  tiktok:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/tiktok.yaml"
    path: ./ruleset/tiktok.yaml
    interval: 86400

  bilibili:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/bilibili.yaml"
    path: ./ruleset/bilibili.yaml
    interval: 86400

  ai:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/ai.yaml"
    path: ./ruleset/ai.yaml
    interval: 86400

  networktest:
    type: http
    behavior: classical
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/networktest.yaml"
    path: ./ruleset/networktest.yaml
    interval: 86400

  applications:
    type: http
    behavior: classical
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/applications.yaml"
    path: ./ruleset/applications.yaml
    interval: 86400

  proxy:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/proxy.yaml"
    path: ./ruleset/proxy.yaml
    interval: 86400

  cn:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/cn.yaml"
    path: ./ruleset/cn.yaml
    interval: 86400

  telegramip:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/telegramip.yaml"
    path: ./ruleset/telegramip.yaml
    interval: 86400

  privateip:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/privateip.yaml"
    path: ./ruleset/privateip.yaml
    interval: 86400

  cnip:
    type: http
    behavior: ipcidr
    url: "https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/cnip.yaml"
    path: ./ruleset/cnip.yaml
    interval: 86400

rules:
  - RULE-SET,ads,🛑 广告拦截
  - RULE-SET,private,🔒 私有网络
  - RULE-SET,microsoft-cn,Ⓜ️ 微软服务
  - RULE-SET,apple-cn,🍎 苹果服务
  - RULE-SET,google-cn,📢 谷歌服务
  - RULE-SET,games-cn,🎮 游戏平台
  - RULE-SET,netflix,🎥 奈飞视频
  - RULE-SET,disney,📽️ 迪士尼+
  - RULE-SET,max,🎞️ Max
  - RULE-SET,primevideo,🎬 Prime Video
  - RULE-SET,appletv,🍎 Apple TV+
  - RULE-SET,youtube,📹 油管视频
  - RULE-SET,tiktok,🎵 TikTok
  - RULE-SET,bilibili,📺 哔哩哔哩
  - RULE-SET,ai,🤖 人工智能
  - RULE-SET,networktest,📈 网络测试
  - RULE-SET,applications,🖥️ 直连软件
  - RULE-SET,proxy,🪜 代理域名
  - RULE-SET,cn,🔗 直连域名
  - RULE-SET,telegramip,📲 电报消息
  - RULE-SET,privateip,🔒 私有网络,no-resolve
  - RULE-SET,cnip,🇨🇳 国内 IP
```
# 三、 导入（以 [Clash Verge](https://github.com/zzzgydi/clash-verge) Windows 端导入 rule-set 规则集为例）
1. 首次使用可进入 Clash Verge->配置，新建“Merge”类型的配置，完成后点击“保存”，右击新建的 Merge 文件，选择“启用”
2. 进入文件夹 *%USERPROFILE%.config\clash-verge\profiles*，找到与第 1 步新建的 Merge 文件相对应的 .yaml 文件，复制其文件名并替换下面命令中的{文件名}；将下面命令中的{DNS 模式}替换为正在使用的 DNS 模式（`fake-ip` 或 `redir-host`）  
以管理员身份打开 CMD 命令提示符，执行如下命令：
```
taskkill /f /t /im "Clash Verge*"
taskkill /f /t /im clash-meta*
curl -o %USERPROFILE%\.config\clash-verge\profiles\{文件名}.yaml -L https://cdn.jsdelivr.net/gh/DustinWin/clash-ruleset@release/{DNS 模式}-user.yaml
```
