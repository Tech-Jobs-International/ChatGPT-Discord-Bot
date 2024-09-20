# ChatGPT Discord Bot
# ChatGPT Discord Bot

中文 | [English](README.en.md)

[![license](https://img.shields.io/pypi/l/ansicolortags.svg)](LICENSE) [![Release](https://img.shields.io/github/v/release/TheExplainthis/ChatGPT-Discord-Bot)](https://github.com/TheExplainthis/ChatGPT-Discord-Bot/releases/)

ChatGPT is integrated into Discord, allowing teams to quickly improve collaboration, communication, and efficiency. By following the installation steps below, you can also introduce ChatGPT into your own Discord.

## Updates
- 2023/03/03 The model was switched to chat completion: `gpt-3.5-turbo`

## Introduction
By introducing the ChatGPT Bot into each channel on Discord, simply type `/chat` in the input box, and a `/chat message` keyword will be automatically filled in. You can directly enter text to interact with ChatGPT, as shown in the image below:  
![Demo](https://github.com/TheExplainthis/ChatGPT-Discord-Bot/blob/main/demo/chatgpt-discord-bot.gif)

## Installation Steps
### Obtaining Tokens
1. Get an API Token from OpenAI:
    1. Register/Log in to the [OpenAI](https://beta.openai.com/) platform.
    2. In the top right, click on your avatar, and select `View API keys`.
    3. Click on `Create new secret key` in the middle.
    - Note: Each API has a free quota and its limitations. For more details, see [OpenAI Pricing](https://openai.com/api/pricing).
2. Get a Discord Token:
    1. Log in to the [Discord Developer](https://discord.com/developers/applications) portal.
    2. Create a bot:
        1. Go to `Applications` on the left.
        2. Click `New Application` in the top right, enter the Bot name, and confirm to go to a new page.
        3. Click `Bot` on the left.
        4. Click `Add Bot` on the right.
        5. Enable `MESSAGE CONTENT INTENT` at the bottom.
        6. Click `Save Changes`.
        7. Get your Token by selecting `View Token` at the top or `Reset Token` if you already applied for one.
    3. Set up OAuth2:
        1. Click `OAuth2` on the left.
        2. Click `URL Generator` on the left.
        3. In `SCOPES` on the right, select `bot`, and under `BOT PERMISSIONS` below, select `Administrator`.
        4. Copy the URL at the bottom and paste it into your browser.
        5. Select the server you want to add the bot to.
        6. Click `Continue` > `Authorize`.

### Project Setup
1. Fork the GitHub project:
    1. Register/Log in to [GitHub](https://github.com/).
    2. Go to the [ChatGPT-Discord-Bot](https://github.com/TheExplainthis/ChatGPT-Discord-Bot) project.
    3. Click `Star` to support the developer.
    4. Click `Fork` to copy all the code to your own repository.
2. Deploy (using free hosting):
    1. Go to [Replit](https://replit.com/).
    2. Click `Sign Up` and log in with your `GitHub` account, then authorize -> click `Skip` to bypass initialization.
    3. In the middle of the main page, click `Create` -> in the pop-up box, click `Import from Github` in the top right.
    4. If GitHub repositories haven't been linked yet, click the link `Connect GitHub to import your private repos.` -> check `Only select repositories` -> select `ChatGPT-Discord-Bot`.
    5. Return to the fourth step, where you can now select the `ChatGPT-Discord-Bot` project -> click `Import from Github`.

### Running the Project
1. Setting Environment Variables:
    1. After completing the `Import`, go to the `Replit` project management page, and click `Secrets` under `Tools` in the lower left.
    2. After clicking `Got it`, you can add environment variables. You need to add the following:
        1. OpenAI API Token:
            - key: `OPENAI_API`
            - value: `[Obtained from step 1] sk-FoXXXX`
        2. Selected model:
            - key: `OPENAI_MODEL_ENGINE`
            - value: `gpt-3.5-turbo`
        3. Role message for the assistant (currently not officially supported, so it's up to the user to test).
            - key: `SYSTEM_MESSAGE`
            - value: `You are a helpful assistant.`
        4. Discord Token:
            - key: `DISCORD_TOKEN`
            - value: `[Obtained from step 1] MTA3NXXX`
2. Start the project:
    1. Click `Run` at the top.
    2. Once successful, the right panel will display `Hello. I am alive!`, and you should copy the URL at the top, which will be needed in the next step.
    - Note: If no requests are made within an hour, the program will stop, so the next step is required.
3. CronJob to send requests periodically:
    1. Register/Log in to [cron-job.org](https://cron-job.org/en/).
    2. In the dashboard, select `CREATE CRONJOB` in the top right.
    3. Enter `ChatGPT-Discord-Bot` as the `Title` and paste the URL from the previous step into the URL field.
    4. Set the time interval to send requests every `5 minutes`.
    5. Click `CREATE`.

## Commands
| Command | Description |
| --- | --- |
| `/chat` | Type `/chat` in the input box, and it will auto-complete with `message`. Enter text to call the ChatGPT model. |
| `/reset` | ChatGPT remembers the last ten conversations. This command clears the history. |
| `/imagine` | Type `/imagine` in the input box, and it will auto-complete with `prompt`. Enter text to call the DALL·E 2 model and generate images. |

## Support Us
If you like this project and want to [support us](https://www.buymeacoffee.com/explainthis), you can buy us a coffee. This will motivate us to keep going!

[<a href="https://www.buymeacoffee.com/explainthis" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="45px" width="162px" alt="Buy Me A Coffee"></a>](https://www.buymeacoffee.com/explainthis)

## Related Projects
- [chatGPT-discord-bot](https://github.com/Zero6992/chatGPT-discord-bot)

## License

[MIT](LICENSE)
