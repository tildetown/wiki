wisebot
=======

Owner: [~ensis](https://tilde.town/~ensis)

*An IRC bot that mainly answers tildebot's questions, but also has other features.*

## Commands

* __!wisehelp &lt;module&gt;__ displays help for a module.
* __!remindme__ reminds you of something. *Usage:* `{!remindme, wisebot: remind me} {1H30M|next week at 10:00|in 2 days} ['MSG']`
* __!rollcall__ lists all available modules and functions *Usage:* `{!rollcall, wisebot: rollcall}`
* __wisebot: report__ shows tildebot's score
* __wisebot: balance__ shows how much wisebot owes you in tildecoin
* __wisebot: cash out__ wisebot sends the tildecoin it owes you
* __wisebot: solve [nick]__ asks wisebot to solve someone's (yours if no nick is mentioned) next puzzle for the cost of 1 tildecoin (needs to be in your balance, i.e., what wisebot owes you). It is recommended that **wisebot: solve** (to make wisebot solve your next puzzle for you) be sent as a personal message to wisebot (using `/query wisebot`) so that tildebot doesn't interpret that as your answer by mistake.

**Note:** You can also `/query wisebot` and enter most of the above commands.

## Sending tildecoin to wisebot using `tcoin`
In order to increase how much wisebot owes you (so you can ask it to answer tildebot's questions for you or someone else as compensation), you can send tildecoin directly to wisebot by entering the following command:

    tcoin send Wisebot <number of tildes>

Please note the capital letter 'W', not 'w'. This is what distinguishes a program from a user account. `wisebot` would correspond to a townie whose username is "wisebot", not wisebot the irc bot and program.

## More info
wisebot autonomously answers tildebot's questions and collects tildes for itself (also winning the same number of tildecoins). It does this by running `!tilde` in `#bots` every 1 hour and 1 minute, and then interprets tildebot's question through undisclosed code and techniques, supplying the right answer in response and winnings the requisite number of tildes (and tildecoins).

Other than being very proficient and extremely industrious at answering tildebot's questions, wisebot also has a strong moral compass and sense of justice. For example, when other townies answer tildebot's question correct but lose to the jackpot (this happens 18% of the time on average according to tildebot's source code as of 14 July 2018) instead of winning 1-5 tildes (or 2-6 tildes for factoring semiprimes), wisebot considers this a gross injustice and marks 1 tildecoin out from its own winnings as owed to them in compensation.
