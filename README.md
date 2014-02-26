Submitting Patches
------------------
Our ROM is open source, and patches are always welcome!
You can send patches by using these commands:

    cd <project>
    <make edits>
    git add -A
    git commit -m "commit message"
    git push ssh://<username>@gerrit.omnirom.org:29418/<project> HEAD:refs/for/<branch>

Register at gerrit.omnirom.org and use the username that you registered there in the above command

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't start a new patch), but instead of git commit -m
use git commit --amend. Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [OMNI ROM Code Review](https://gerrit.omnirom.org)


Getting Started
---------------

To get started with OMNI ROM, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

To initialize your local repository using the OMNIROM trees, use a command like this:

    repo init -u git://github.com/omnirom/android.git -b <branch>

Then to sync up:

    repo sync

Then to build:

     cd <source-dir>; . build/envsetup.sh; brunch <device_name>


If you need more information or a more detailed guide, click [here to see our wiki.](http://docs.omnirom.org)

Our official IRC Channels are hosted on Freenode:

[#omnirom - USERS](http://webchat.freenode.net/?channels=omnirom/)

[#omni - DEVELOPERS](http://webchat.freenode.net/?channels=omni/)

