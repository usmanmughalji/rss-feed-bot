# RSS to Telegram bot

A self-hosted telegram python bot that dumps posts from RSS feeds to a telegram chat. This script was created because all the third party services were unreliable.

![Image of help menu](https://bokker.github.io/telegram.png)

# Installation

## On Local Machine (WSL - Ubuntu)

- Install Python 3.8.x

- Clone this repo:
```
git clone https://github.com/usmanmughalji/rss-feed-bot
cd rss-feed-bot
```
- Install dependencies for running setup scripts:
```
pip3 install -r requirements.txt
```
## Setting up config file
```
cp config_sample.env config.env
```

Fill up rest of the fields. Meaning of each fields are discussed below:
- **BOT_TOKEN** : The telegram bot token that you get from `@BotFather`
- **CHAT_ID** : Add chat id, to get this chat id follow this method, add `@GoogleIMGBot` to the group, and send /id in the chat to get this value.
- **DELAY** : Default value is 60 seconds, you can change if you want.

**Warning!** Without chatID the bot wont be able to send automated messages and will only be able to respond to messages.

- Now Run Bot:
```
python3 telegramRSSbot.py
```
## For Quick and Easy Installation

## Click Here!

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/usmanmughalji/rss-feed-bot/tree/master)

# Usage

send /help to the bot to get this message:

> RSS to Telegram bot
>
> After successfully adding a RSS link, the bot starts fetching the feed every 60 seconds. (This can be set)
> Titles are used to easily manage RSS feeds and need to contain only one word
>
> commands:
>
> **/add** title http://www(.)URL(.)com
>
> **/help** Shows this text
>
> **/remove** !Title! removes the RSS link
>
> **/list** Lists all the titles and the RSS links from the DB
>
> **/test** Inbuilt command that fetches a post from Reddits RSS.
>
> The current chatId is: 20416xxxx

## Updates

- Updated Requirements
- Added Heroku Support Properly

# Known issues

If the bot is set to for example 5 minutes and one feed manages to get 2 new posts before the bot can check. Only the newest post will show up on telegram.

## Credits, and Thanks to
* [BoKKeR](https://github.com/BoKKeR/RSS-to-Telegram-Bot) For His Wonderful Code (Original Repo)
* [Usman Mughal](https://github.com/usmanmughalji) Hmm
