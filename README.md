## Submitting Patches ##
------------------
To prevent missue of gerrit - yes unfortunately there are poeple
out there that do such things - it is required to be registered as
contributor to submit changes. So if you want to submit patches
contact us by email to <admin@omnirom.net> with your gerrit
username and/or email so we can add you to this group.

Our ROM is open source, and patches are always welcome!
You can send patches by using these commands:

    cd <project>
    <make edits>
    git add -A
    git commit -m "commit message"
    git push ssh://<username>@maxwen.ddns.net:29418/<project> HEAD:refs/for/android-14.0

Register at <maxwen.ddns.net> and use the username that you registered there in the above command

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't start a new patch), but instead of git commit -m
use git commit --amend. Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [OmniROM Code Review](https://maxwen.ddns.net)


## Maintaining Authorship ##
----------------------
Maintaining authorship is a very important aspect of working with Open Source code. If you wish to submit a patch/fix
from anywhere else (another ROM, project, etc.), it is imperative that you maintain the ownership of the person whose
work you are seeking to include. Doing so will ensure that credit is given where it is deserved, and the [prinicples of open source](http://opensource.org/docs/osd)
are upheld. Your contribution to the project will still be recognized as you will forever be listed as the committer.

If you manually cherry pick a patch/fix then you will need to add the original author prior to pushing to our [gerrit](https://maxwen.ddns.net).
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

To get started with OmniROM, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

To initialize your local repository using the OmniROM trees, use a command like this:

    repo init -u https://github.com/omnirom/android.git -b android-14.0

Then to sync up:

    repo sync

Then to build:

     cd <source-dir>; . build/envsetup.sh; brunch <device_name>

## Private Repositories ##
---------------

The repositories in omni-private are only accessible to registered users
So if you want to use those please contact us by email to <admin@omnirom.net>
with a short description what you want to use them for. Send us your github
account then we can add you to the group that has read access to those
repositories.

Changes to those repositories are still accessible on gerrit

You can also build without those repositories if you dont need or
want the features that are in them. In that case simply remove the include

    <include name="omni-private.xml" />

## Qcom Repositories ##
---------------

Most of Qcom repo are moved to our [Gitlab](https://gitlab.com/omnirom), like Display.
Here, you can find an eg how to add this repo into your dependencies

```bash
   {
     "remote": "gitlab",
     "repository": "android_vendor_qcom_opensource_display-commonsys",
     "target_path": "vendor/qcom/opensource/commonsys/display",
     "revision": "android-12.0"
   }
```