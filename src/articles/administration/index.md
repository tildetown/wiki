# tilde.town administration

This page covers all aspects of tilde.town administration. Its primary goal is
to serve as a complete guide to running tilde.town. While morbid, imagine that
[~vilmibm](/~vilmibm) shuffled off the mortal coil tomorrow: without this
document, the running of the town would be a big mystery.

Its secondary goal is to provide a guide to *volunteer admins*, users who have
some limited scope of administrative privilege. They help take the burden off of
~vilmibm.

Its final goal is to promote transparency. The town is best described as
anarcho-monarchist society: users self-govern according to the
[coc](/wiki/conduct.html), appealing to an all-powerful admin (~vilmibm) if
self-governance hits a wall. Such an arrangement benefits from administrative
transparency, for without trust in the admin the limits of self governance can
undermine the community (for example, not being able to ban a repeat coc
violator).


## Root

The town's `root` account is accessible only to ~vilmibm and two emergency
admins: [~cmr](/~cmr) and [~datagrok](/~datagrok). In the past, sudo has been
granted to some deputized users for a short term (like [~karlen](/~karlen),
[~demophoon](/~demophoon), and [~krowbar](/~krowbar)).

`root` sees all and can do all. It has access to every single file and can assume
any user at any time. **This is a big deal**. In general, actions that are not
strictly required to be run as `root` should not and are not run as `root`. Users
are not monitored in any way and their files are only examined in the course of
fixing a system issue (ie, a runaway script) or conduct violation (ie, improper
use of system resources or harassment).

## The admin group

Some resources are owned by the `admin` group. This group exists to help
volunteer admins access certain system resources without being granted root
privileges. This group is not heavily used at the moment, but exists and will be
used as the volunteer admin program expands.

## The Admin App

About a year ago, ~vilmibm was feeling a tremendous amount of pressure keeping
the town going. Adding users required `root` access and there was no easy way to
share the responsibilities; worse, adding users was a heavily manual process.

Thus, ~vilmibm wrote [the django admin
app](https://github.com/tildetown/tildetown-admin). This is a web GUI that:

- Runs a guestbook available to the public
- Runs a helpdesk system available to the public
- Exposes a user sign up page to the public
    - that can validate RSA and RSA keys
    - that can ensure uniqueness of usernames
    - that provides a basic CAPTCHA
- Exposes a private admin interface that:
    - can add and update user accounts on disk
    - can post to social media
    - can triage help tickets
    - can moderate the guestbook

It was instrumental in keeping tilde.town alive. Now, it automates most of what
~vilmibm used to shell in and become `root` to do manually and has made administration of the town much easier.

It has also opened up an opportunity to have volunteer admins with a very restricted permission set. The admin app accomplishes this with:

- Django Admin's group and permission system
- a dedicated user on the system (`ttadmin`)
- A carefully crafted set of [scripts](https://github.com/tildetown/tildetown-admin/tree/master/scripts) and [sudoers](https://help.ubuntu.com/community/Sudoers) entries

## Volunteer admins

Volunteer admins are people who assist ~vilmibm with tasks regular users are not
permitted to perform but that don't require full `root` access. In addition to serving as operators for the `#tildetown` IRC channel (the default one), they are allowed
to log into the admin app and take various actions there. They are marked as
"staff" and put in the *Volunteer Admins* group, which has the following
permissions:

- Delete guestbook messages
- Add or update help tickets
- Update users (rename them or fix their information)
- Add public keys to users

Volunteer admins **CANNOT**:

- edit the content of guestbook messages
- delete help tickets
- delete users
- delete public keys

Currently they don't receive special privileges on tilde.town itself, though
this will opefully change.

The current volunteer admins:

- [~karlen](/~karlen)
- [~l0010o0001l](/~l0010o0001l)
- [~archangelic](/~archangelic)

If you'd like to volunteer, you can send a local email to `vilmibm@tilde.town`.
However, the volunteer admin program is still in beta, and at the moment new
folks might not be approved.

## IRC administration

Our IRC server is bare bones. We don't run NickServ or ChanServ and haven't
really needed to (we still probably should though). The `#tildetown` channel
(where you appear when you run `chat`) is the only "official" channel; in other
words, the only users with special privileges there are ~vilmibm and the
volunteer admins.


## Volunteer Admin Handbook

This section details the various responsibilities of a volunteer admin.

### Field helpdesk tickets

- Login to [https://cgi.tilde.town/admin]
- Click on Tickets
- Click on a ticket marked **to triage**
- If the ticket asks for something you can do, update the ticket's status to **Acknowledged** and then do it. Once you're done, mark it as **Nothing more to do**.
- If you don't have the permission to do the task (ie install new software) or don't understand it, leave the status alone and tell ~vilmibm about it.
- If a user needs to be updated on the status of their ticket, send them a personal email. I usually use the subject "tilde town ticket!"
- If the ticket is something you can do but you're blocked on more info from the user, update its status to **waiting to hear from submitter**.

### Add a new user

Users sign up via the [sign up form](https://cgi.tilde.town/users/signup). They
are created in the admin app's database, but will not exist on the actual server
until an admin approves them.

To review and add a user:

- Login to [https://cgi.tilde.town/admin]
- Click on Townies
- For each user account, check their information:
    - Does their email already have an account here? (see related [issue](https://github.com/tildetown/tildetown-admin/issues/31))
    - Do their reasons seem weird? An empty reasons box is fine, but are they trolling?
    - Is there anything suspicious about their email?
- From the townie list, select the users you want to approve with the checkbox on the left.
- In the **Action:** drop down, select **Mark selected townies as reviewed.** This:
    - creates the user on disk
    - announces the new users on mastodon and twitter
    - sends each user a personal email
- Verify: 
    - that they are marked as reviewed (green checkmark) in the Townies list
    - the announcement went out on [mastodon](https://tiny.tilde.website/@tildetown)
    - the announcement went out on [twitter](https://twitter.com/tildetown)

### Add a public key for a user

- Login to [https://cgi.tilde.town/admin]
- Click on Townies
- Find the user (searching for their username works) and click on them
- Scroll to the **PUBKEYS** section
- In the first open **Pubkey object** box:
    - Select the pubkey type (probably `ssh-rsa`)
    - Paste in the pubkey
- Scroll down and click **SAVE**

You should probably let the user know this is done.


### Rename a user

Should a user request a rename in a help desk ticket, the process is:

- Is the new username taken? Stop and let them know via email if so.
- Login to [https://cgi.tilde.town/admin]
- Click on Townies
- Find the user (searching for their username works) and click on them
- Update their "username" field.
- Click save. This will:
    - run `usermod` to rename the user
    - move their home directory to match their new name
  
You should probably let the user know this is done.


### Moderate the guestbook

- Login to [https://cgi.tilde.town/admin]
- Click on **Guestbook messages**
- For any messages that are obviously spam (and not funny or tasteful enough to keep), select them with the checkbox to the left
- In the **Action:** dropdown, select **Delete selected guestbook messages**.

### Set IRC topic

in `#tildetown`, run `/topic this is my cool new topic`

### Restore ops to someone

If a volunteer admin (or ~vilmibm themself) loses operator status for some reason, help them out with `/op username` in the `#tildetown` channel.


## Admin Only Tasks

### Run chsh or chfn for a user

Currently, if users want a shell other than bash they have to ask an admin to do it since users do not get passwords on tilde.town (and the `chsh` program requires a password).

This [should be
automated](https://github.com/tildetown/tildetown-admin/issues/29), either as a
volunteer admin task or a self-service tool.

### Install new software

Only root can run `apt`. If you want software installed, file a help ticket.

### Ban a user

This is extremely rare. The "ban" process is:

- `rm -rf /home/banned_user`
- `deluser banned_user`
- deleting the user from the admin app database.

### Create disk backups

This task is performed from the AWS console, which only ~vilmibm has access to.

### Audit user activity

This is more common than banning a user but still very rare. This involves
running `find` on a user's home directory to find questionable things or
investigate high disk usage or possibly reading a user's command history file.

### Manage services

The services that `root` is responsible for (and, for example, might need
restarting if the server restarts):

- bbj
- admin app
- irc (charybdis)
- mail server
- postgresql
- nginx

### Manage Starbound

Our shared Starbound server runs on a different server than tilde.town proper.
Only ~vilmibm can log into it and use root there.
