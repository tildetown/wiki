# File Permissions

File permissions, also known as _access modes_, determine who can access and
modify files. On the command line you can list files along with their
permissions with `ls -l`, and you can change file permissions using the `chmod`
command.

In a directory listing, permissions appear by default as a sequence of ten
characters, something like `drwx------` or `-rw-rw-r--`, for instance.

Here's an example directory listing -- the first column shows the file permissions:

<pre>
    $ ls -l
    drwxrwxr-x  4 bart bart   4096 Oct 27 21:41 ./
    drwxr-xr-x 23 bart bart   4096 Oct 27 21:30 ../
    -rw-rw-r--  1 bart staff     0 Oct 15 22:01 foo
    drwxrwxr-x  2 bart bart   4096 Oct 27 21:41 public/
    drwx------  2 bart bart   4096 Oct 27 21:40 secrets/
    -rw-rw----  1 bart staff     7 Oct 15 22:01 wibble
</pre>

The very first character shows whether or not the file is a directory. (That first character has other uses too, but we won't cover that here.) The next nine characters represent the actual file permissions. If you split those nine characters into three 3-character sequences, you get the permissions for 1) the file owner, 2) group members, and 3) everyone else.

<pre>
         g   o
     u   r   t
     s   o   h
     e   u   e
     r   p   r

    rwx rwx rwx   <-- read, write, execute (or directory access)
    421 421 421       these equate to the octal bits 4, 2, and 1 respectively
</pre>

The characters `r`, `w`, and `x` represent read access, write access, and permission to execute the file as a program (or to grant directory access if the file is a directory).

In the example directory listing above:

* `foo` is a file that can be read by anyone, but only written to by `bart` or members of the `staff` group.
* `public` is a directory that anyone can access, but only `bart` can modify.
* `secrets` is a directory that only `bart` can access.
* `wibble` is a file that `bart` and any `staff` member can acess and modify, but nobody else can access at all.

(Be aware that system administrators can access files regardless of file permissions. Permissions can help manage files, but aren't about absolute privacy.)


## Using `chmod` to modify file permissions

The `chmod` command understands two equivalent access mode formats:

<pre>
    chmod u=rw,g=,o= FILENAME(s)     chmod u=rwx,g=,o= FILENAME(s)
    chmod 600 FILENAME(s)            chmod 700 FILENAME(s)

    chmod u=rw,g=r,o= FILENAME(s)    chmod u=rwx,g=rx,o=rx FILENAME(s)
    chmod 640 FILENAME(s)            chmod 755 FILENAME(s)

    chmod r=rw,g=rw,o=r FILENAME(s)
    chmod 664 FILENAME(s)
</pre>

Those octal values can be derived by adding the relevant octal bits. Some common examples:

<pre>
    rw- --- ---    rw- r-- ---    rw- rw- r--    rwx --- ---    rwx r-x r-x
    42- --- ---    42- 4-- ---    42- 42- 4--    421 --- ---    421 4-1 4-1
     6   0   0      6   4   0      6   6   4      7   0   0      7   5   5
</pre>

See the `chmod` manual page (`man chmod`) for more information. The related
`chown` and `chgrp` commands can be used to manage file ownership.

