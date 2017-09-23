irssi
=====

## Setting up a mentions/hilight window for irssi.

If you run irssi in a screen you might miss mentions and it's time
consuming to scroll back through logs looking for them.

A better way is to create a mentions or hilight window dedicated to
any messages that contain your nickname.

(instructions adopted from [here](https://quadpoint.org/articles/irssi/)).

Install cras's hilightwin.pl:

```
mkdir -p ~/.irssi/scripts/autorun
curl -L https://github.com/irssi/scripts.irssi.org/raw/gh-pages/scripts/hilightwin.pl > ~/.irssi/scripts/autorun/hilightwin.pl
```

Setup the hilight window

```
/window new split
/window name hilight
/window size 6
/layout save
```

Load script

```
/script load autorun/hilightwin.pl
```

## away_screen.pl

`away_screen.pl` is a script for irssi which automatically sets `/away` when you detach from screen.
It can also automatically change your nickname when you detach from screen so you can let others
know when you're away. It will also log mentions you've received while detached.

### Installation

```
# download screen_away.pl
curl http://scripts.irssi.org/scripts/screen_away.pl ~/.irssi/scripts

# (optional) autoload it by symlinking to ~/.irssi/scripts/autorun
# you may need to make the autorun directory first
cd ~/.irssi/scripts/autorun && ln -sv ../screen_away.pl .

# restart irssi in a screen
```

To automatically change your nickname when detached, run the following command from irssi:

```
/set screen_away_nick YOUR_AWAY_NICKNAME
````
