## Submitting Patches ##
------------------
Our ROM is open source, and patches are always welcome!
You can send patches by using these commands:

    cd <project>
    <make edits>
    git add -A
    git commit -m "commit message"
    git push ssh://<username>@gerrit.omnirom.org:29418/<project> HEAD:refs/for/android-5.1

Register at gerrit.omnirom.org and use the username that you registered there in the above command

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't start a new patch), but instead of git commit -m
use git commit --amend. Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [OMNI ROM Code Review](https://gerrit.omnirom.org)


## Maintaining Authorship ##
----------------------
Mainting authorship is a very important aspect of working with Open Source code. If you wish to submit a patch/fix
from anywhere else (another ROM, project, etc.), it is imperative that you maintain the ownership of the person whose
work you're seeking to include. Doing so will ensure that credit is given where it is deserved, and the [prinicples of open source](http://opensource.org/docs/osd)
are upheld. Your contribution to the project will still be recognized as you will forever be listed as the committer.

If you manually cherry pick a patch/fix then you will need to add the original author prior to pushing to our [gerrit](https://gerrit.omnirom.org).
This is a very easy task to perform, and is usually done after you commit a patch/fix locally. This is accomplished
after you type in `git commit -a` , type in the commit message and save. You would then do the following:

```bash
git commit --amend --author "Author <email@address.com>"
```

So it should look like this once you get all of the author's information

```bash
git commit --amend --author "Spencer McGillicuddy <spencer.the.bestest@gmail.com>"
```

Alternatively, adding as part of the original `git commit` message is preferred and done like the following:

```bash
git commit --author="Author <email@address.com>" -m "[commit message]"
```

This saves time, and when part of your normal routine, prevents the infamous "ermahgerd I forgot to add authorship -
let me fix it because I was found out!" message.


## Getting Started ##
---------------

To get started with OMNI ROM, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

To initialize your local repository using the OMNIROM trees, use a command like this:

    repo init -u git://github.com/omnirom/android.git -b android-5.1

Then to sync up:

    repo sync

Then to build:

     cd <source-dir>; . build/envsetup.sh; brunch <device_name>


If you need more information or a more detailed guide, click [here to see our wiki.](http://docs.omnirom.org)

Our official IRC Channels are hosted on Freenode:

[#omnirom - USERS](http://webchat.freenode.net/?channels=omnirom/)

[#omni - DEVELOPERS](http://webchat.freenode.net/?channels=omni/)
