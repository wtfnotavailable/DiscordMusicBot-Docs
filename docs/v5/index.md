---
title: v5 - Latest
description: This is Discord Music Bot version 5 documentation.
---

<h1 style="font-family:Nunito Sans;font-size: 2.0em;font-weight: bold;color: white;">Discord Music Bot version 5</h1>

!!! danger "Discord Music Bot is not compatible with Lavalink v4"

    v4 introduce a breaking changes that affects all library that are using v3 API. You must update your bot library to support v4!
    See [github.com/wtfnotavailable/Discord-MusicBot/issues/201](https://github.com/wtfnotavailable/Discord-MusicBot/issues/201) regarding Lavalink v4 compatibility.


## 🚧 | Prerequisites

- [Docker](https://www.docker.com/)
- Optionally: [GNU Make](https://www.gnu.org/software/make/)

## 📝 | Tutorial

### Written Setup

- Follow the [installation](/v5/getting-started/) procedure for the bot
    - Do keep in mind that this is the ONLY part of the tutorial that you need to follow from the original repo, which is the core of the bot

#### For everything else:
- Make sure you have [Docker](https://www.docker.com/) (and [GNU Make](https://www.gnu.org/software/make/)) installed on your machine
  - If you are planning on running the bot through docker on windows, then you'll have to use WSL and set up the appropriate docker configurations for that [(click here)](https://docs.docker.com/desktop/windows/wsl/)
- Open a terminal session in in the root directory of the project
- Run `make help` to see the list of available commands
  - If you don't have or can't install makefile utilities then run `./dc.sh help`
  - If you're having trouble running the script due to lack of permissions be sure to `chmod +x dc.sh`

#### Docker setup

- Run `make up` to start the docker environment with all services active
  - Use `make up help` for a list of available sub commands
- Run `make log` to see the logs of all services at once
  - You can exit them at any time without closing the process by pressing `Ctrl + C`
- If you don't want a particular service to start up on `make up` you can simply add a `no` flag to the command. For example:
  - `make up nodb` will start the docker environment without the DB.
  - `make up noll` will start the docker environment without the lavalink server.
  - `make up nofe` will start the docker environment without the frontend.
  > Note: you can use any combination of the flags above to start the docker environment with only the services you want.

#### Lite version

The bot also supports a lite version to run the bot without docker. This is useful for development and testing purposes as well as potato machines.
- Run `make lite help` for a list of available sub commands
Contrary to the `make up` command, the `make lite` command will only start the bot, without any additional services.
- To add additional services you can use the `make lite` with the following flags:
  - `make lite db` to start the DB
  - `make lite ll` to start the lavalink server
  - `make lite fe` to start the frontend

#### Local setup

- Run `make up no-docker` to start the bot locally (on your maching, without virtualization and thus extended services)

- Run `make up help` to see the list of available commands and options
- Remember to remove the DB related environment variables from the `./djs-bot/.env` file if you are not using the DB at all.

## 📝 | [Support Server](https://discord.gg/sbySMS7m3v)

If you have major coding issues with this bot, please join and ask for help.

## 📸 | Screenshots

Soon

## 🚀 | Deploy

- No deployment options have been configured yet

## ✨ | Contributors

Contributions are always welcomed :D Make sure to follow [Contributing.md](/CONTRIBUTING.md)

<a href="https://github.com/SudhanPlayz/Discord-MusicBot/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=SudhanPlayz/Discord-MusicBot" />
</a>

## 🌟 | Made with

- [Discord.js](https://discord.js.org/)
- [Lavalink](https://github.com/freyacodes/Lavalink) with erela.js, Cosmicord.js