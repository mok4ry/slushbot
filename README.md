# slushbot

[![Circle CI](https://circleci.com/gh/rit-sse/slushbot.svg?style=svg)](https://circleci.com/gh/rit-sse/slushbot)

Part Bot, Part Slash Command, Part who knows what?

## Developing

### Getting Started

The only way to realy test out things right now is to really use it in slack so I recommend creating a slack team for yourself to use for testing.
I'm going to try to figure out a local solution later.

For this slack team, you will need to add 2 integrations:
* A Slash command `/sse`
* A bot user

After you set those up, run the bot

*Note*: This bot needs to be publically accessable for the slash commands to work so open up the port or deploy it somewhere.

* `npm install`
* `token=[YOUR SLACK BOT TOKEN] npm start`

If you go to your slack team, you should see the bot user is online and you are able to run the existing slash commands

### Creating a New Command

1. Assess whether you should be creating a bot command or a slash command. Genrally SSE related and anything that warrents a private response should be a slash command. Anything that requires the bot to be in the channel should be a bot command.  If you aren't sure right off the back, ask on the corresponding issue.
2. `npm run create -- --name [script name] --type [bot|slash]` This will create a file for you to work in.
3. Make your script. I recomend looking at the existing scripts of the type as well as the [botkit](https://github.com/howdyai/botkit) and [slack](https://api.slack.com) documentation for guidance.
4. Make a pull request
