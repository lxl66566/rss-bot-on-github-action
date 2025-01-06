# RSS bot on github action

English | [简体中文](./README.zh-CN.md)

> [!CAUTION]
> This is a test repo for the following scenario. However, due to limitations in the [rssbot](https://github.com/iovxw/rssbot) itself, this scenario does not work. In other words, **the code in this repository does not work!!!!** If you can fix this, I will gratefully accept your PR!

<details><summary>Preface</summary>

I don't like running RSS feeds on my host; I think chat software is a good carrier for RSS, and the chat software I use most often is Telegram, so I've been using Telegram's RSS bot.

One day, the RSS bot I was using was delayed for several days; I tried to replace it with another RSS bot, and got the reply ‘the global maximum number of subscriptions has been reached, please try to build your own’.

My own servers are yearly or monthly throwaway machines, so I didn't want to build a bot on an unstable machine. years of ~~abuse~~ of Github Actions suddenly gave me an inspiration: why not build an RSS bot on Github Actions? This once-in-a-while service is perfect for running on Github.

</details>

A RSS to Telegram bot runs on Github Action.

## Usage

1. Fork repo。
2. Add your Telegram bot token named as `BOT_TOKEN` to Secrets。
3. Delete `rssbot.json`。
4. Enable workflow in _Actions_。
5. Send command to your Telegram bot, refer to [here](https://github.com/iovxw/rssbot).
6. Wait it to run and reply. Or you can run it manually.

Other：

- Runs 1 min per 10 hours by default. To adjust the behavoir, edit `.github/workflows/fetch.yaml`.
