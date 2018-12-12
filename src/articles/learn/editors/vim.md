# vim quickstart

The core concept of `vim` is _modal editing_, where you are in one of a few
modes while editing text. The modes determine what happens when you press
keys.

The most important mode to know is _Insert Mode_, which lets you type things.
The default mode is _Normal Mode_, where you can edit the text that is already
there or run commands.

When you start `vim`, press `i`. You should see **-- INSERT --** at the bottom
of your screen. You can now type away happily.

When it's time to save, hit `escape`. The escape key is used in vim to exit
whatever mode you are in; thus, from insert mode, you go back to normal mode.

Now press `:`. In normal mode, this opens a little command line at the bottom
of your screen. Type `w` and hit `enter`. You just saved your file.

To quit, make sure you are in normal mode. press `:`, type `q`, and hit enter.

If you've made an edit, you wont be able to quite using just `:q`, though.  If
you want to abandon your changes, use `:`, and then type `q!`, and then hit
enter.  To save changes,  use `:`, and then type `wq`, and then hit enter.

For a more in depth tutorial on vim, check out this cool [interactive
tutorial](http://www.openvim.com/).

Our own ~shanx has [a page](/~shanx/vim.html#TIL) about `vim`, as does [~kirch](/~kirch/vim.html).
