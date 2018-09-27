botany over IRC
===============

[~eeeeeta](/~eeeeeta/index.html) wrote a script that lets you control your
botany plant over IRC!

## disclaimer

You may wish to back up your botany data before using this script. ~eeeeeta
doesn't think it does anything bad, but they don't know how python works,
so it's probably better to be safe.
To do so, run:

```
$ cp -rv ~/.botany ~/.botany.bak
```

You can then move the `~/.botany.bak` folder back to its original place if
things go south.

## usage instructions

To use the script, run:

```
$ ~eeeeeta/botanyirc.sh localhost OWNER BOTNICK
```

Replace `OWNER` with your IRC nickname, and `BOTNICK` with the IRC nickname
you want the bot to use. If all goes well, you will then receive some
`/NOTICE`s on IRC from the bot, showing you your plant's status in much the
same way as regular botany. Here's an example of what the bot's output looks
like:

<pre>
12:06 -- etabotany: ---  botany  ---
12:06 -- etabotany: commands: water, look, garden, visit, instructions, exit
12:06 -- etabotany: plant: young jade plant
12:06 -- etabotany: score: 545750
12:06 -- etabotany: water ())))))))))) 99% 
12:06 -- etabotany:           .    ,
12:06 -- etabotany:           o%O %,o
12:06 -- etabotany:            \%o'
12:06 -- etabotany: .  , _ . ., l, _ ., _ .
12:06 -- etabotany:   ^      '        `    '
</pre>

To control the plant, simply reply with one of the `commands` that the bot
offers you. Please note that the `garden` and `visit` commands are yet to be
implemented.

Feel free to yell at ~eeeeeta over IRC/alpine/whatever if you have questions!
