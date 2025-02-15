# ChatGPT Telegram Bot
### see [announcement thread on twitter](https://twitter.com/altryne/status/1598822052760195072)

- Uses your local browser using Playwright to run chatGPT in chromium
- Sends messages
- Parses code and text
- has a `/draw` command in telegram to draw pictures using stable diffusion!
- more stuff coming after I rest

![CleanShot 2022-12-02 at 16 08 27](https://user-images.githubusercontent.com/463317/205404516-56ea908e-dd31-4c53-acb7-15f9f6ed379f.gif)


# How to install

* Make sure that python and virtual environment is installed.

* Create a conda environment with `conda env create -f environment.yml`. (If this fails you might need to set your path, using this command: `export PATH="/path/to/conda/bin:$PATH"`)

* If you are installing playwright for the first time, it will ask you to run this command for one time only to download all the chrome software
```
playwright install
```

You need to setup your telegram bot token [how to](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and [user id](https://bigone.zendesk.com/hc/en-us/articles/360008014894-How-to-get-the-Telegram-user-ID-) in `.env` file.
Edit the .env.example file and rename it to .env and place your values in there.

This version named [server2.py](https://github.com/seichris/chatGPT-telegram-bot/blob/main/server.py) allows you to add multiple Telegram ids to your env vars, in the following format:
`TELEGRAM_USER_ID=123456,654321,876543`

Edit the file using `nano /etc/xrdp/chatGPT-telegram-bot/.env`

* Now run the server

```
conda activate chat
python server.py
```

Then find your bot in telegram (you should have already created it with @botfather) and start chatting.

# Credit

* Got started with this using [Daniel Gross's whatsapp gpt](https://github.com/danielgross/whatsapp-gpt) package.


# How to run it on a server instead of locally

- Set up an ubuntu Server
- Install xrdp
- Start xrdp
- `git copy` this repo
- Remote desktop into this server
- Log into a GUI instance of xrdp
- Run the above commands from this readme to set up your telegram bot
- Auth in your remote desktop window
