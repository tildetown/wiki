# How to edit your HTML homepage

Your `public_html` directory is the place to store HTML (i.e. web pages) and
associated files you'd like to make publicly available on the World Wide Web.
Your tilde.town account includes a default place-holder web page -- it can be
visited using a web browser:

`https://tilde.town/~YOUR_USER_NAME/index.html`

That `index.html` file is actually located in your `public_html` directory.

To edit it, log in to your tilde.town account using
[ssh](../getting-started/ssh.html) and open the file in a
text editor -- for example,
[nano](../learn/editors/nano.html):

```
$ nano ~/public_html/index.html
```

In `nano`, editing commands are listed at the bottom of the screen. When you
see a `^` character, that indicates the Ctrl key. So, for example, `^O Write Out`
means press Ctrl-O to save your work, and `^X Exit` means press Ctrl-X to exit.
([Help with other editors](../learn/editors/quick-ref.html).)

You're not limited to a single HTML file in your `public_html` directory: you
can add more web pages, along with stylesheets, images, subdirectories, etc.
But `index.html` is the page people will see by default if they visit
`https://tilde.town/~YOUR_USER_NAME/` without specifying any other file.

If you have a file in your `public_html` directory that can't be accessed via a
web browser, chances are it's a file permission problem. Using the `chmod`
command to make the file readable to anyone will likely fix it:

```
$ chmod u=rw,g=r,o=r ~/public_html/FILENAME
```

As well as editing files over `ssh`, you can upload and download files using a
related tool called `sftp` (...which you run at _your_ end, as with `ssh`). For
the manual, type `man sftp` and see especially the _Description_ and
_Interactive Commands_ sections. Some of the most useful `sftp` commands are:

```
help             Show a list of sftp commands
ls [PATH]        Show a directory listing from the remote computer
lls [PATH]       Show a directory listing from the local computer
cd PATH          Change the current remote directory to PATH
lcd PATH         Change the current local directory to PATH
put FILE         Copy FILE from the local computer to the remote computer
get FILE         Copy FILE from the remote computer to the local computer
mput FILES       Copy multiple files from the local computer to the remote computer
                 For example, to upload all JPG files: mput *.jpg
mget FILES       Copy multiple files from the remote computer to the local computer
                 For example, to download all HTML files: mget *.html
rename OLD NEW   Rename OLD as NEW on the remote computer
mkdir PATH       Create the named directory on the remote computer
rmdir PATH       Delete the named directory on the remote computer
rm FILE          Delete the named file on the remote computer
pwd              Show the current working directory on the remote computer
lpwd             Show the current working directory on the local computer
bye              Quit sftp
```

Some useful resources:

* [Learn HTML](https://www.w3schools.com/)
* [Learn CSS](https://www.w3schools.com/css/default.asp)

