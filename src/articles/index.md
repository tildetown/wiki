# welcome to tilde.town's wiki!

the tilde.town wiki houses our server-specific documentation, pages about
various art projects, guides on linux, fiction, and other wonderful content.

## navigating

check out the [table of contents](toc.html) for all the pages, or [around
town](around-town.html) for a summary of things to do!

## how to contribute to the wiki

all users can edit this wiki. from your home directory, run:

    wiki init

and follow the prompts. once it's done, you can edit the files, add new files,
or create and populate new directories. check the changes you make with:

    wiki preview
    w3m tilde.town/~YOU/wiki

where `YOU` is your username.

when you are happy with your changes, run

    wiki publish
    w3m tilde.town/wiki

sometimes, you might get conflicts with changes other people have made. for
now, fall back on git commands to fix it. if this is unfamiliar to you, ask in
IRC (via the `chat` command) or in the forum (via `bbj`) and someone will
definitely help you.

to view wiki pages from the command line, run

    wiki get editors/micro

to list the contents of the wiki, run

    wiki get toc

to sync the contents of your version of the wiki with the published version, run

    wiki sync

as always on the town, folks are here to help each other. if you run into
problems feel free to ask for help. and maybe document the answer on the wiki
for the next person :D
