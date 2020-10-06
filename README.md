<p align="center">
<img src="https://i.loli.net/2018/10/30/5bd7b06b077df.png" width="200px">
</p>
<h1 align="center">Cloudflare Block Bad Bot Ruleset</h1>

<p align="center">
<a href="https://github.com/SukkaW" target="_blank"><img alt="Author" src="https://img.shields.io/badge/Author-Sukka-b68469.svg?style=flat-square"/></a>
<a href="./LICENSE" target="_blank"><img alt="License" src="https://img.shields.io/github/license/sukkaw/cloudflare-block-bad-bot-rules.svg?style=flat-square"/></a>
</p>

> Block bad, possibly even malicious web crawlers (automated bots) using Cloudflare Firewall Rules<br>
> 使用 Cloudflare Firewall Rules 拦截恶意网络爬虫（自动机器人）和其它恶意流量

## Introduction 简介

`Cloudflare Block Bad Bot Ruleset` projects stop and block Bad Bot, Spam Referrer, Adware, Malware and any other kinds of bad internet traffic ever reaching your web sites. Inspired by [nginx-badbot-blocker](https://github.com/mariusv/nginx-badbot-blocker) & worked with Cloudflare Firewall Rules.

`Cloudflare Block Bad Bot Ruleset` 可以阻止恶意爬虫、垃圾引荐来源、广告、恶意软件以及任何其他类型的恶意互联网流量到达您的网站。灵感来自 [nginx-badbot-blocker](https://github.com/mariusv/nginx-badbot-blocker) 并与 Cloudflare Firewall Rules 搭配使用。

## Precautions 注意事项

`Cloudflare Block Bad Bot Ruleset` mainly based on User-Agent, which is known to all that could be changed easily. So the project can not replace the Web Application Firewall.

`Cloudflare Block Bad Bot Ruleset` 主要基于 User-Agent，但是众所周知 User-Agent 可以伪装，所以本项目并不能取代正规的 Web Application Firewall。

## Ruleset 规则

Rule Name | File Name | Action | What For
---- | ---- | ---- | ----
Good Bot | [good-bot.rules](./good-bot.rules) | Allow | Match known good bot.<br>匹配已知的正常爬虫
IDC ASN List | [idcasnlist.rules](./idcasnlist.rules) | JS Challenge | Based on known partial IDC ASN number.<br>基于已知的部分IDC ASN号（包含阿里云盾）
Basic Crawler | [basic-crawler.rules](./basic-crawler.rules) | Block/Challenge | Block some known bad bot.<br>匹配一些基本的 HTTP Request 库
Bad Crawler | [bad-crawler.rules](./bad-crawler.rules) | Block/Challenge | Match mostly known bad bot, basic ruleset not included.<br>匹配绝大部分已知的恶意爬虫

## Usage 用法

![](https://i.loli.net/2018/10/30/5bd801833e8d3.png) 

ASN规则可在防火墙→工具→IP访问规则处添加，不占用宝贵的可使用规则条数。

## More Information 更多详情

- [Announcing Firewall Rules | Cloudflare Blog](https://blog.cloudflare.com/announcing-firewall-rules/)
- [Cloudflare Firewall Rules | Cloudflare Documentations](https://developers.cloudflare.com/firewall/)
- [nginx-badbot-blocker | GitHub](https://github.com/mariusv/nginx-badbot-blocker)
- [nginx-ultimate-bad-bot-blocker | GitHub](https://github.com/mitchellkrogza/nginx-ultimate-bad-bot-blocker)

## Todo List

- [ ] Bad referrer list
- [ ] Known bad IP List

## Maintainer 维护者

**Cloudflare Block Bad Bot Ruleset** Made By [Sukka](https://github.com/SukkaW) Modified By [Dumeng](https://github.com/XMD0718), Released under the [MIT](./LICENSE) License.