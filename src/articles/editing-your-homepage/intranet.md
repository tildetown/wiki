# tilde.town intranet

There is an informal intranet on tilde.town accessible at `localhost:12345`. 
You can either access the intranet locally after logging into tilde.town 
using [lynx](https://linux.die.net/man/1/lynx), [w3m](https://linux.die.net/man/1/w3m) or a similar text-based web browser,
or you can use `ssh`'s local port forwarding to remotely access the intranet from your favorite web browser.

## How to add pages to your intranet

Simply create a `private_html` directory in your home directory.

<code><pre>
cd ~
mkdir private_html
</pre></code>

Then, go into your `private_html` and add HTML files just like you would 
in `public_html`. The latter is for the internet (public for the world 
to see) and the former is for the intranet (only other townies can see 
them).

## How to use the intranet as startup page in your text-based browser

In order to automatically access the intranet when launching e.g. lynx from your shell,
you can make use of the WWW_HOME environment variable by adding it to your shell config.
Details vary however and depend on your respective shell. In the case of bash, add
`export WWW_HOME='http://localhost:12345/'`
to either your `.bash_profile` or `.bashrc` file, whichever one you use,
then reload your config by running `source .bash_profile` or `source .bashrc`. 
The next time you launch your browser of choice from the shell, the intranet landing page should appear.

## How to connect to the intranet remotely


add the following block to ~/.ssh/config on your local machine (create it if it doesn't exist)

<code><pre>
Host town
  Hostname tilde.town
  User your_username_here
  LocalForward localhost:12345 localhost:12345
  ServerAliveInterval 240
</pre></code>

then on your local machine, you can simply run `ssh town` and a magical intertube will be created
for you to visit the tildtranet along with your normal shell session.
the magical intertube will close as soon as your shell session does.

try this link: [http://localhost:12345/~login/](http://localhost:12345/~login/)

alternately, you can type in this magical incantation if you don't want to bother with ssh_config

`ssh -L 12345:localhost:12345 your_username_here@tilde.town`

---

another option is to use some scripts to manage your ssh tunnel:

Two very simple scripts placed in a convenient directory are all you 
need to switch on and switch off your connection to tilde.town's 
intranet. You should run these scripts using the same terminal you use 
to log into tilde.town. [More information about using ssh to log into 
tilde.town.](https://tilde.town/wiki/ssh.html)

Make sure you save these files and run `chmod u+x <filename>` to make 
them executable. Then run the first one (`./ttci`) when you need 
to connect to the intranet and the second one (`./ttciend`) when you 
want to disconnect from the intranet.


The first one is called `ttci` (tilde.town connect intranet):

<code><pre>
\#!/bin/bash
\#ttci = tilde.town connect intranet
ssh -N your_username_here@tilde.town -o ServerAliveInterval=240 -L localhost:12345:localhost:12345 -i 
~/.ssh/your_private_key_file &
echo $! > ~/.ssh/ssh_pid
</code></pre>

The second one is called `ttciend` (tilde.town connect intranet end):

<code><pre>
\#!/bin/bash
if [ -e ~/.ssh/ssh_pid ] 
then
  kill `cat ~/.ssh/ssh_pid`
  rm ~/.ssh/ssh_pid
fi
</code></pre>

## How to browse the intranet

Once you've run `ttci` to connect, instead of going to 
`https://tilde.town/~endorphant/` you should go to 
`http://localhost:12345/~endorphant/` to browse ~endorphant's 
intranet home page.

Once you run `ttciend`, the URLs with `localhost:12345` in 
them will stop working since you will have disconnected from the 
intranet. You can run `ttci` to connect again.

I hope you enjoy tilde.town's intranet!
