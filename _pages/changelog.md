---
layout: page
title: What's New
include_in_header: true
---

# Changelog

### `Latest`
# **Version 1.1.1**

#### What's New
- Emojis can be disabled by sending EMOJIS
  ![no-emojis](/assets/changelog/no-emojis.PNG)

#### Bug Fixes
- Mishandled multiple occurrences of letters all in the wrong spot.  Thanks, Bri!

#### TODO
- Ensure selected word of the day can't be repeated.
- Curate a list of possible words for the day (as opposed to choosing from the dictionary)
- Find a cheaper alternative to Twilio SMS while keeping the core texting feature.

<br>

### **Version 1.1  | Feb 22, 2022**

#### What's New
- Added ASCII-keyboard to show how many letters are available
![ASCII-keyboard](/assets/changelog/keyboard.jpg)

#### Bug Fixes

<br>

________
<br>

### `Initial Release`
# **Version 1.0  | Feb 18, 2022**
- Winning the game of the day now tells how many people failed!
![loses](/assets/changelog/lost.jpg)

#### Bug Fixes
- Losing returned the last word guessed instead of the correct word.  Thanks, Jilli!
- Textle was attempting to respond to images and message reactions.  These are now ignored.  Thank you, Mom!
- Game creation endpoint was not firing (changed from GET to POST)

<br>

## **Version 0.2  | Feb 17, 2022**
Textle is now hosted on Google App Engine using a Mongo as a database.  GAE has a < 2 second wake-up (as opposed to Heroku's 15s) and gives a $300 credit.  Luckily (as if by design), Textle has extremely low CPU utilization meaning I'm spending close to $0 a month.  For the future, I need to watch memory usage as I pull the dictionary of words into memory.  I'm using MongoDB because I hate databases and wanted to give it a go.  It was also free.

#### What's New
- Textle is now hosted on Google App Engine
- Data is stored using MongoDB
- Moved from APScheduler to Cloud Scheduler for notification and game creation.

<br>

## Version 0.1  | Feb 15, 2022
On February 15th at 12:05am, I heard someone spoil the Wordle in the school library.  After seeing a video on TikTok of people emulating Wordle, I realized how easy it would be to make a bot to play the game over text.

#### What's New
- Conversation states to keep track of user progress in games and conversation:
  - sign-up flow
  - opt-in/out for game notifications
  - game errors (word length, doesn't exist)
  - solved/failed
- Twilio integration for playing the game via text
- In-memory database (which is a fancy way of saying there is no database, just a dictionary full of phone number to user object mappings)

<br>