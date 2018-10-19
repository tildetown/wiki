# How to edit your HTML homepage

Your `public_html` directory is the place to store HTML (i.e. web pages) and associated files you'd like to make publicly available on the World Wide Web. Your tilde.town account includes a default place-holder web page -- it can be visited using a web browser:

`https://tilde.town/~YOUR_USER_NAME/index.html`

As mentioned, that `index.html` file is actually stored in your `public_html` directory.

To edit it, log in to your tilde.town account using [ssh](https://tilde.town/wiki/getting-started/ssh.html) and open the file in a text editor -- for example, [nano](https://tilde.town/wiki/learn/editors/nano.html):

```
$ nano ~/public_html/index.html
```

In `nano`, editing commands are listed at the bottom of the screen. When you see a `^` character, that indicates the Ctrl key. So, for example, `^O Write Out` means press Ctrl-O to save your work, and `^X Exit` means press Ctrl-X to exit.

You're not limited to a single HTML file in your `public_html` directory: you can add more web pages, along with stylesheets, images, etc. But `index.html` is the page people will see by default if they visit `https://tilde.town/~YOUR_USER_NAME/` without specifying any other file.

As well as editing files over `ssh`, you can upload and download files using a related tool called `sftp` (...which you run at _your_ end, as with `ssh`). For the manual, type `man sftp` and see especially the _Description_ and _Interactive Commands_ sections.

Some useful resources:

* [Learn HTML](https://www.w3schools.com/)
* [Learn CSS](https://www.w3schools.com/css/default.asp)

