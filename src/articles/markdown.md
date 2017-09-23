# Markdown

Why write HTML by hand when you can write [Markdown](http://commonmark.org/) easily on your tilde.town server?

Three simple steps:

1. write your wiki page as a markdown file and save it with a `.text` extension. eg: `markdown.text`
2. type `make` in the shell. The `markdown.text` file + `page.theme` will be turned into `markdown.html` page.
3. add these two files to git via `git add markdown.text markdown.html` and commit.
4. profit!

## Markdown Syntax

Reference: [Markdown Basics](http://daringfireball.net/projects/markdown/basics)

    Major Header
    ============

    Minor header
    ------------

    # Alternative Format Major Header

    ## Alternative Format Minor header

    ### Even more minor header

    > Block quote

    *italics* or _italics_

    **bold** or __bold__

    * Unor-
    * dered
    * List
    * (may also use + or - for bullets)

    1. Or-
    2. dered
    3. List

    [link text](link URI)

    ![alt text](image-URI "image title")

    `code` (or indent paragraph four spaces or tab)

### Results

Major Header
============

Minor header
------------

# Alternative Format Major Header

## Alternative Format Minor header

### Even more minor header

> Block quote

*italics* or _italics_

**bold** or __bold__

* Unor-
* dered
* List
* (may also use + or - for bullets)

1. Or-
2. dered
3. List

[link text](link URI)

![alt text](image-URI "image title")

`code` (or indent paragraph four spaces or tab)




