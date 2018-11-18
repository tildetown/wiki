Gopher Wiki
============

[Gopher](https://en.wikipedia.org/wiki/Gopher_(protocol)) is a pre-web internet protocol based on a hierarchy of menus and documents.
See below for useful links and clients for Gopher.

To get started with Gopher on the town, make a `public_gopher` directory in your home and it will be listed on the main menu of [gopher://tilde.town](gopher://tilde.town).
You can start immediately by putting various files and directories in your `public_gopher`, and they will be displayed on Gopher.
In addition, you can create a file named `gophermap` to add information, links, and labels for files. 

## `gophermap` format

`gophermap` contains tab-separated data, for example

    0My text file	file1.txt
    1My dir	funfiles

The first line contains two columns: `0My text file` and `file1.txt`.
The second column points to a (local) file, while the first column
contains the description that will appear in the menu ("My text
file"), as well as the *item type* (`0`, stands for text files).  You
can find the list of item types and their associated codes in the
table below.

The second line contains a link to a subdirectory `funfiles` with the
description `My dir`. The item type in this case is `1`, which stands
for a directory or a Gopher submenu. You also use the same item type
for providing links to Gopher menus on other servers:

    1The official frogs.tips gopher hole	/	gopher.frogs.tips	70

This entry contains three more columns: the item selector (aka, the
path on the server), the host name of the server, and the desired port
(which defaults to 70 for Gopher). Using the same scheme you can link
to text files and other kinds of items on different servers.

The item type "i" enables inline text in your gophermap:

    iThis text will be displayed as is. This will not be rendered as a link.

See [this tutorial](https://gopher.zone/posts/how-to-gophermap/) on
gophermap written by 'cat'. Also available on gopher:
[gopher://baud.baby/0/phlog/fs20181102.txt](gopher://baud.baby/0/phlog/fs20181102.txt).

**Item types**

    0     Text file
    1     Directory/Gopher submenu
    2     CSO name server
    3     Error
    4     Mac HQX filer
    5     PC binary
    6     UNIX uuencoded file
    7     Search server
    8     Telnet Session
    9     Binary File
    g     GIF image
    h     HTML, Hypertext Markup Language (useful for the WWW URLs)
    i     "inline" text type
    s     Sound
    I     Image (other than GIF)
    M     MIME multipart/mixed message


## Clients

Gopher can be accessed directly from your tilde.town shell with some text-based web browsers, like `lynx` or `w3m`, by specifying the desired protocol.

Example: `lynx gopher://tilde.town`

There is a variety of gopher clients around, and it's even possible to browse gopher directly with telnet/netcat.
Some popular clients are:

- [Overbite](https://gopher.floodgap.com/overbite/)
- [VF-1](https://github.com/solderpunk/VF-1)

## References and external links

[2007 Gopherspace Mirror](https://archive.org/details/2007-gopher-mirror)

[A video on Gopher](https://www.youtube.com/watch?v=JbJKf0UOGAc)

[SDF Gophermap Guide](http://sdf.org/?tutorials/gopher)

[SDF Gophermap Guide Archive](https://web.archive.org/web/20101005063208/)
