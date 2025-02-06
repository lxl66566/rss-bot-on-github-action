# RSS bot on github action

[English](./README.md) | 简体中文

这是一个运行在 Github Action 上的 RSS Telegram bot。

> [!CAUTION]
> 这是以下设想的测试 repo。不过由于 [rssbot](https://github.com/iovxw/rssbot) 本身功能的限制，该设想无法正常工作。也就是说，**这个仓库的代码无法正常使用！！！**  
> **请前往 [Telegram-RSS-Bot-on-Cloudflare-Workers](https://github.com/lxl66566/Telegram-RSS-Bot-on-Cloudflare-Workers)**，这是我后来写的项目，它可以正常在 Cloudflare Workers 上运行 Telegram bot，订阅 RSS 并发送更新通知，无需服务器部署。

## 前言

我不喜欢在主机上跑 RSS 订阅软件；我认为聊天软件是 RSS 的一个很好的载体，而我最常用的聊天软件是 Telegram，因此我一直在用 Telegram 的 RSS bot。

某一天，我常用的那个 RSS bot 出现了延迟多日的情况；尝试更换另一个 RSS bot，得到回复 “已达到全局最大订阅数量，请尝试自建”。

我自己的服务器都是年抛或月抛机，因此我并不想在不稳定的机器上搭建 bot。多年~~滥用~~ Github Actions 的经验突然带给了我一个灵感：为什么不在 Github Actions 上搭一个 RSS bot 呢？这种一段时间运行一次的服务非常适合在 Github 上跑。

## 使用

1. fork 此仓库。
2. 在 Secret 里添加名为 `BOT_TOKEN` 的 Telegram bot token。
3. 删除仓库内的 `rssbot.json`。
4. 在 Actions 界面，启用 workflow。
5. 按照 [这里](https://github.com/iovxw/rssbot) 的说明，对您的 Telegram 机器人发送订阅指令。
6. 等待其自动运行，并响应指令。或者也可以手动运行。

其他：

- 默认每 10 小时运行一次，每次 1 分钟。如需修改请自行调整 `.github/workflows/fetch.yaml`。
