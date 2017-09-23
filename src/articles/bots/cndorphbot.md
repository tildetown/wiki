cndorphbot
==========

owner: [~endorphant](http://tilde.town/~endorphant) | [source](http://tilde.town/~endorphant/cndorphbot.py.txt)

*A personal bot friend.*

## Features

* _Automatic tilde mining;_ when activated, asks for a !tilde at intervals of at least 60 minutes, and defeats the tildebot arithmetic captcha by performing some text processing.
* _Channel haunting;_ summons the ghost of a user by loading lines from the #tildetown IRC log, then repeating them chronologically at a randomish interval. When it runs out of lines, the ghost dissipates.
* _Internet time;_ reports the current [beat](https://en.wikipedia.org/wiki/Swatch_Internet_Time) to the nearest thousandth.

## Commands

* __!beat__ gives the current beal meridian time
* __!tildeboard__ gives the top five !tilde scores, according to the tildebot records
* __!leaderboard__ does the same, without triggering the tildebot
* __!exhume *{username}* *{yyyy-mm-dd}*__ loads lines from username on given date (logs start 2014-12-29)
* __!silphscope__ reveals current ghost
* __!banish__ instantly ends haunting

Responds to the following when directly addressed ("__cndorphbot: *{message}*__")

* <3
* tildeboard
* botsnack
* time/mark/sync (old debugging commands, left in for flavor)
* report (calls !tildescore)
* beg (asks for a !tilde)
