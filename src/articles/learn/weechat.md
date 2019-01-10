weechat
=======

Do you prefer **irssi**? [Check it out here!](irssi.html)

## Some tricks in weechat

0. You can scroll through a buffer (called browsing the scrollback) by using the *Page Down* and *Page Up* keys. On macOS with keyboards that don't have those buttons, this is **Fn + Up Arrow Key** (**Page Up**) to scroll up and **Fn + Down Arrow Key** (**Page Down**) to scroll down.

1. You can go through your direct mentions (called highlights because the name of the person who mentioned you is highlighted, usually with a bright background) using **Alt + P** (for previous) and **Alt + N** (for next).

2. You can go to a buffer (what look like "tabs" in weechat are called buffers) numbered **&lt;n&gt;** using **/buffer &lt;n&gt;**.

25. You can move the current buffer to the position of the **&lt;n&gt;**th buffer (and shift the rest of them to the right by one unit) using **/buffer move &lt;n&gt;**.

26. You can swap two buffers numbered **&lt;m&gt;** and **&lt;n&gt;** using **/buffer swap &lt;m&gt; &lt;n&gt;**.

3. You can go to a buffer numbered **&lt;n&gt;** (where **&lt;n&gt;** is between 1 and 10) using **Alt + &lt;n&gt;** (**&lt;n&gt;** is 0 for the buffer numbered 10).

4. You can go from one buffer to the next using **Alt + Down Arrow Key** and **Alt + Up Arrow Key**, as well as **Alt + &gt;** (**Alt + Shift + .**) and **Alt + &lt;** (**Alt + Shift + ,**).

5. A unified buffer is that where what would belong in separate buffers are shown together in a single buffer (with a single number). A common example of a unified buffer is one where weechat's core buffer (which always opens when you run weechat and cannot be closed) and server buffers (which is where the irc server's responses to server-directed commands like **/list** appear) are shown together. One can switch between buffers (sub-buffers?) in a unified buffer using **Ctrl + X**.

6. One can autocomplete usernames by typing part of the username, then pressing **Tab**.

7. One can view an easily copyable version of messages in the buffer by pressing **Alt + L**. This is good for things like copying hyperlinks or quoting an irc conversation in a blog post.

8. **/list** will list all the channels on the server with more than a couple of participants.

9. **/join #channelname** will start a new channel called #channelname if none existed, and will make you join it (and open it in a new buffer).

10. **/close** will close a buffer (and leave a channel if you didn't already **/leave**).

11. **/quit** will disconnect all connected servers close weechat, and is the most-asked-about command about weechat (or any other irc client for that matter).

12. **/query &lt;nickname&gt;** will start a private conversation with &lt;nickname&gt;.

13. **/nick &lt;new-nickname&gt;** will change your old nickname to &lt;new-nickname&gt; Please use this command carefully, because it will free your old nickname up and you might not be able to get it back easily if someone else changes their nickname to it.

14. **/msg &lt;nickname&gt; &lt;msg&gt;** will start a private conversation with &lt;nickname&gt; and automatically send them a message with contents &lt;msg&gt;.

15. **/disconnect** will disconnect from the server whose channel the current buffer holds.

16. **/connect &lt;server-name&gt;** will connect to a server with name &lt;server-name&gt;.

17. **/server add &lt;server-name&gt; &lt;server-url&gt;** will add a server with those properties to weechat. Only after a server is added can one **/connect** to it.

18. **/set** sets options. For example, **/set irc.server.&lt;server-name&gt;.command "/msg nickserv identify xxxxxx"** will make weechat execute the command in quotes when &lt;server-name&gt; is joined.

19. **/set buflist.look.enabled 1** enables the buffer list on the left, and **/set buflist.look.enabled 0** disables the same.

20. **F9** to scroll Weechat's title bar (with the topic in it) to the left, and **F10** to scroll it to the right.

21. **Ctrl + P** to go to the previous channel on the buffer list, and **Ctrl + N** to go to the next channel on the buffer list.

More information here: <https://weechat.org/files/doc/devel/weechat_quickstart.en.html>.
