# How to edit your `public_html`

Your `public_html` directory is the place to store HTML (i.e. web pages) and associated files you'd like to make publicly available on the World Wide Web. Your tilde.town account includes a default web page - it can be visited using a web browser:

`https://tilde.town/~YOUR_USER_NAME/index.html`

That `index.html` file is stored in your `public_html` directory.

To edit it, log in to your account using [ssh](https://tilde.town/wiki/getting-started/ssh.html) and open that file in a text editor -- for example, [nano](https://tilde.town/wiki/learn/editors/nano.html):

```
$ nano ~/public_html/index.html
```

(Note: in `nano`, editing commands are listed at the bottom of the screen. When you see a `^` character, that means the Ctrl key. So, for example, `^X Exit` means press Ctrl-X to exit.)

Of course, you're not limited to a single page. You can add more, along with stylesheets, etc.

As well as editing files over `ssh`, you can upload and download files using a related tool called `sftp`.

Some useful resources:

* [Learn HTML](https://www.w3schools.com/)
* [Learn CSS](https://www.w3schools.com/css/default.asp)

