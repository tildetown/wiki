# editors

Inevitably, you're going to want to edit a file on tilde.town. It might be a
beautiful pile of HTML, a poem, or some delicious spaghetti code. If you're
used to editing files on a graphical desktop it can be kind of daunting to
accomplish this task at first.

This part of the wiki covers the editors we have available on the town, ranked
by beginner friendliness.


## protip!

A lot of documentation on editors (and command line programs in general) tells
you about key combinations you can use. While in a graphical desktop you have
the ability to either click on `File -> Save` or hit `C-s`, here we just have
the latter.

So when you see `C-s`, that means _hold control and press s, then release_.

If you see `S-C-s`, that means _hold shift and control, press s, then release_ You probably won't
see `S-s` since that just means S.

The somewhat confusing `M-x` means _hold alt, press x, then release_.

You might also see `C-c C-x` Which means _hold control and press c, release c, press x, release both keys_.

**You might also** see the charcter `^` used to mean _hold control_.

## let's do this

1. nano

    `nano` can't do much, but what it can do it makes very easy and straightforward.

        nano public_html/index.html

    All of the operations (saving, quitting) are shown whenever you run `nano`,
    making it self-documented. It's definitely a go-to editor if you're brand new
    to editing text in a command line environment.

    Our own ~minerobber has [a page](/~minerobber/nanoreference) about `nano`.

2. micro

    While `micro` is very simple, you do have to do a little more learning than
    `nano`. You'll be rewarded with more features, though, like split screens and
    syntax highlighting.

        micro public_html/index.html

    `micro` is intended for beginners and is easy to get going with. Check out our
    page on [micro](micro.html) for a reference on how to use it.

3. emacs

    `emacs` has been around for a long time and can do many, many things. It's
    also easy to extend with your own features, making its list of features
    essentially infinite. There is a pretty steep learning curve for emacs, but
    for basic text editing you can get the hang of it pretty quick.

        emacs public_html/index.html

    Check out [our quickstart](emacs.html) to learn more.

4. vim

    In many ways `vim` is simpler than `emacs`, but it takes an approach to text
    editing called _modal editing_ that sets it apart from the other editors on
    this list. This approach is pretty sweet but is not for everyone and takes
    time to get used to.

        vim public_html/index.html

    Check out [our quickstart](vim.html) to learn more.

5. everything else

    We have more editors than just the ones listed above, but they are of more
    interest to those curious about Unix history or obscure software. Check out
    [~elly's tutorial](https://tilde.town/~elly/ed.html) on `ed` or, from the
    command line, run `man joe`.
