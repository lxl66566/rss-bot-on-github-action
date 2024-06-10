# RSS bot on github action

English | [简体中文](./README.zh-CN.md)

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
