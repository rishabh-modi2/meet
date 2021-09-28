telegram meet

It is a telegram bot which can be deployed to a server, heroku or on your local machine. It can attend your Google Meet and Zoom classes for you. You can also schedule meetings and it will automatically join at the given time.

also read https://github.com/rishabh-modi2/meet/blob/master/PLEASE_READ_THIS.md

## Bot Commands

    /help - Show avaliable commands
    /meet - Command to join Google Meet classes or metting
    /zoom - Command to join Zoom Meeting
    /status - Sends screenshot of the web page
    /exit - Exit Meeting
    /timatable - Shows todays meeting schedule
    
## Usage
	
	Join Google Meeting
    /meet https://meet.google.com/agr-ghts-ade
    
    Get list of commands
    /help
    
    Join Zoom Meeting
    /zoom 12354674654 ax56rR
	
    Get screenshot of the web page
    /status

    Exit Google Meet or Zoom Meeting
    /exit

	If you've set SCHEDULER in config.py to True

	Use /timetable to get todays schedule

**BOT_TOKEN** : You can get the BOT TOKEN from Bot Father on Telegram. [Here is a guide on how to create and new bot and get it's BOT_TOKEN](https://www.siteguarding.com/en/how-to-get-telegram-bot-api-token)

**SCHEDULER** :  If you want to use scheduler on bot set this to `TRUE` else set it to `False`

**USERID** : Set this to your Telegram User ID. ( You can use @userinfobot on Telegram for that )

## Setup Scheduler
> If you want to use Scheduler set SCHEDULER to True in [config.py]https://github.com/rishabh-modi2/meet/blob/schedule/config.py)

1. cd meet
2. cd bot
3. python3 [schedule.py](https://github.com/rishabh-modi2/meet/blob/schedule/bot/schedule.py)

The scheduler.py script will guide you to setup schedule for your meetings. It stores the schedule in a CSV file. 


## Deploy to Linux Machine and Linux Server

You would need:

1. Geckodriver and Firefox installed on your system.
2. Python 3.7+ and pip3 installed.

To run it locally:

1. `git clone https://github.com/rishabh-modi2/meet.git`
2. `cd meet`
3. `python3 -m pip install -r requirements.txt`
4. Rename `meet/config.py` to something else.
5. Rename `meet/RunLocallyConfig.py` to `config.py` .
6. Rename `meet/bot/__init__.py` to something else.
7. Rename `meet/bot/RunlocallyInit.py` to `__init__.py` .
8. Set your `USERID`, `BOT_TOKEN` and `SCHEDULE` value in `config.py` .
9. ( You can get your `USERID` from @userinfobot from Telegram, and `BOT_TOKEN` from @BotFather from Telegram. )
10. `python3 chromium.py`

## Deploy to Heroku



You would need :
1. Firefox, for making a profile your meet app will use.
2. [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli#download-and-install) and [Heroku Account](https://www.heroku.com). 
3. Git installed.
4. Some patience.
5. For remaining instructions, please read [this](https://github.com/rishabh-modi2/meet/blob/master/PLEASE_READ_THIS.md). or, watch video tutorials we posted on the telegram group.


## Managing Heroku's Dynos so that your bot won't stop at near the end of the month 

Heroku gives 500 hours/month for free 

And, a month has 720 hours 

So, your app would probably stop working earlier than the end of the month 

To prevent that, you can 

`heroku ps:scale worker=0`

When you're not using it, that command will stop the app

And again, when you want to start it , 

`heroku ps:scale worker=1`

Stopping app when you are not using it, will save hours/month (heroku calls it dynos) for you, so you won't have to redeploy, or will have to wake up early for classes when the end of month is near :)

Also, you can do this ( turning app off or on ) right from your phone on Termux ( Turning on PC just for this might be pain in ass for some people ), so, if you don't know much regarding this, and you want a tutorial, you can ask me out on t.me/siriyourdad



for any problem contact me at t.me/siriyourdad 0r @siriyourdad on telegram
