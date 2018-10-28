Gopher Wiki
============

[Gopher](https://en.wikipedia.org/wiki/Gopher_(protocol)) is a pre-web internet protocol based on a hierarchy of menus and documents.
See below for useful links and clients for Gopher.

To get started with Gopher on the town, make a `public_gopher` directory in your home and it will be listed on the main menu of [gopher://tilde.town](gopher://tilde.town).
You can start immediately by putting various files and directories in your `public_gopher`, and they will be displayed on Gopher.
In addition, you can create a file named `gophermap` to add information, links, and labels for files. 

## `gophermap` format

**How to Edit Gopher Map**

    1.0     Text file
    2.1     Directory
    3.2     CSO name server
    4.3     Error
    5.4     Mac HQX filer
    6.5     PC binary
    7.6     UNIX uuencoded file
    8.7     Search server
    9.8     Telnet Session
    10.9    Binary File
    11.c    Calendar (not in 2.06)
    12.e    Event (not in 2.06)
    13.g    GIF image
    14.h    HTML, Hypertext Markup Language
    15.i    "inline" text type
    16.s    Sound
    17.I    Image (other than GIF)
    18.M    MIME multipart/mixed message
    19.T    TN3270 Session/

**Gopher Map Example**

    Welcome to my Gopher page!
    
    0My text file   file1.txt
    9My pdf file    file2.pdf
    1My dir dir
    
    1.0Why is Gopher Still Relevant?        /gopher/relevance.txt   gopher.floodgap.com     70
    2.hAn http link URL:http://tilde.town/

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
