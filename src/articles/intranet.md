# tilde.town intranet

There is an informal intranet on tilde.town accessible at 
`localhost:12345`. You can access this after logging into tilde.town 
using [lynx](https://linux.die.net/man/1/lynx), or you can use `ssh`'s 
local port forwarding to acess the intranet from your favorite web 
browser.

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

## How to access the intranet

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
#!/bin/bash
#ttci = tilde.town connect intranet
ssh -N login@tilde.town -L localhost:12345:localhost:12345 -i 
~/.ssh/tilde.town &
echo $! > ssh_pid
</code></pre>

The second one is called `ttciend` (tilde.town connect intranet end):

<code><pre>
#!/bin/bash
if [ -e ssh_pid ] 
then
  kill `cat ssh_pid`
  rm ssh_pid
fi
</code></pre>

Once you've run `ttci` to connect, instead of going to 
`https://tilde.town/~endorphant/` you should go to 
`http://localhost:12345/~endorphant/` to browse ~endorphant's 
intranet home page.

Once you run `ttciend`, the URLs with `localhost` in 
them will stop working since you will have disconnected from the 
intranet. You can run `ttci` to connect again.

I hope you enjoy tilde.town's intranet!
