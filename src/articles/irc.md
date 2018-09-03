irc
===

tilde.town has a local irc server! please abide by the
[code of conduct](https://tilde.town/wiki/conduct.html), and contact a
moderator if you have problems. volunteer moderators are designated as ops in
the main channel (they'll have an '@' in front of their name)

the `chat` command will automatically start an irc client ([weechat](weechat.html)) and
connect to the server. if you have opinions about irc clients, you can also
use [irssi](irssi.html).

## irc channels

When you run `chat` you automatically join our main chat, `#tildetown`. You
can join other channels by typing commands like this:

    /join #bots
    /join #music
    /join #tildetown

An incomplete list of channels, sorted by activity:

* *#tildetown*: main general chat; pretty much any topic is welcome here, but
  noisy/intense discussions may be asked to be moved to one of the more
  topic-specific channels
* *#bots*: ircbots/games; can be extremely noisy at times as people test out
  bots
* *#projects*: talk about what sort of creative endeavors you're working on
* *#dumpsterfire*: political/current events/controversial topics; venting and
  heated discussions
* *#engines*: cars, motorcycles, machine nerds, etc.
* *#music*: share songs, talk about music
* *#abookclub*: discussions about books/reading
* *#witches*
* *#tildeplays*
* *#go*: discussion about the board game go/weiqi/baduk; includes a crude ascii
  goban bot
* *#tokipona*: tokipona-language learning/practice/discussion; non-tokipona
  language use is welcome, fluency not necessary
* *#ttbp*: dev updates, troubleshooting, etc. for the feels engine


## tildeverse irc

~town is also part of a wider network of tildes: [tilde.chat](https://tilde.chat).
the tilde.chat network is run by member nodes (currently ~town, tilde.team, and yourtilde.com)
and exists as a place to share and collaborate with other tilde members.

to connect, you can use the configuration settings on the [tilde.chat](https://tilde.chat) site and connect
with those credentials.

or, you can follow these steps to connect through the ~town node:

in chat (which is weechat btw):
<pre><code>
/server add tildeverse 127.0.0.1/7766
/connect tildeverse
</code></pre>

the main channel of the tildeverse is `#meta`, which you can join after
connecting to the network (`/join #meta`).

connecting through the town node grants you access to the town-only channel #town. besides the other
local channels on each member node, all other channels are shared across tildes and will be visible to
other tilde members.

tilde.chat has the same expectations of culture and sharing and kindness as the internal irc chat.
come share the love :)


## irc bots

see the [irc bots wiki page](bots/ircbots.html)
for more information about bots.
