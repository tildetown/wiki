real time chatting with IRC
===

tilde.town has a local IRC server which is the primary means of real-time
interaction on the town (though not the only one). please abide by the [code
of conduct](../../conduct.html), and contact a moderator if you have problems.
volunteer moderators are designated as ops in the main channel (they'll have
an '@' in front of their name)

It's strongly recommended that you check out our [etiquette
guide](../../etiquette.html).

the `chat` command will automatically start an IRC client
([weechat](../../learn/weechat.html)) and connect to the server. if you have
opinions about IRC clients, you can also use [irssi](../../learn/irssi.html).

## channels

our chat is divided up into "channels" which are reflect various topics of
conversation. Channel names are prefixed with a "#" symbol.

When you run `chat` you automatically join our main chat, `#tildetown`. You
can join other channels by typing commands like this:

    /join #bots
    /join #music
    /join #tildetown

An incomplete list of channels, sorted by activity:

* *#tildetown*: main general chat; pretty much any topic is welcome here, but
  noisy/intense discussions may be asked to be moved to one of the more
  topic-specific channels
* *#bots*: IRCbots/games; can be extremely noisy at times as people test out
  bots
* *#projects*: talk about what sort of creative endeavors you're working on
* *#tildemush*: discuss development of the town's in progress MUSH
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
* *#math*: talk about mathematics (at any level) - needs to be more popular than it currently is
* [*#mafia*](channels/mafia.html) - A good old-fashioned game of Mafia.
## IRC Bots

Our chat is full of bots. They range from funny to useful to occasionally
hostile. See the [irc bots wiki page](list-of-bots.html) for more information
about bots.

## Registering your nickname

Registering your nickname in IRC is recommended. It means that no one can
impersonate you in chat. While the likelihood of that is probably low, you can
start to rely on a registered nick to automatically gain moderation powers in
certain channels.

To register a nick, run:

    /quote NS REGISTER yournick your@email.com a-safe-password

updating `yournick`, `your@email.com`, and `a-safe-password` accordingly.

You'll have to set up your client to log you in, however, and it's a little
confusing.

While running chat, press `alt 1`. then run:

    /set irc.server.town.sasl_username yournick
    /set irc.server.town.sasl_password a-safe-password

If this doesn't work, it might be because the server is known as `localhost`
to your weechat. You can either quit and run `chat` again (and then redo the
above steps) or run:

    /set irc.server.localhost.sasl_username yournick
    /set irc.server.localhost.sasl_password a-safe-password

If you customized your weechat config (or you don't use the `chat` command),
this still might fail for you. In that case feel free to ask in chat for help.

## Registering a channel

Registering a channel makes our IRC server remember that channels exist
without people having to be in them and across restarts. Our "permanent"
channels like #tildetown and #bots are registered so their topics stay the
same even if the whole server is restarted.

If you have `operator` status on a channel (that little @ in front of your
name) you might want to register your channel for yourself.

Run this:

    /quote CS REGISTER #yourchannel

replacing `yourchannel` with the name of your channel. Now, you'll be
automatically made an operator when you join the channel and any topic that
is set will be remembered.


## tildeverse IRC

~town is also part of a wider network of tildes:
[tilde.chat](https://tilde.chat). The tilde.chat network is run by member nodes
(currently ~town, tilde.team, and yourtilde.com) and exists as a place to share
and collaborate with other tilde members.

To connect, you can use the configuration settings on the
[tilde.chat](https://tilde.chat) site and connect with those credentials.

or, you can follow these steps to connect through the ~town node:

In chat (a wrapper around weechat):

```
/server add tildeverse 127.0.0.1/7766 -autoconnect
/connect tildeverse
```

The main channel of the tildeverse is `#meta`, which you can join after
connecting to the network (`/join #meta`).

Connecting through the town node grants you access to the town-only channel
`#town`. All other channels are shared across tildes and will be visible to
other tilde members.

tilde.chat has the same expectations of culture and sharing and kindness as
the internal IRC chat. Come share the love. :)

## How to stay connected

If you're tired of disconnecting and reconnecting to chat, you have a few
options.

You can start using the command `tmux` or `shell` to preserve your session on
tilde.town. [Here's a
guide](https://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/) to `tmux`.

You can also do a more advanced thing to get IRC connected directly to your
computer (instead of via ssh). This is called [SSH
tunneling](https://tilde.town/~nick/sshtunnel.html).
