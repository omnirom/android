Submitting Patches
------------------
Our project is open source, and patches are always welcome!
You can send patches by using:

Pull request, right here on git.

Contact me on irc, Network: freenode, Channel: #twrp

Getting Started
---------------

To get started with OMNI sources to build TWRP, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

To initialize your local repository using the OMNIROM trees to build TWRP, use a command like this:

    repo init -u git://github.com/lj50036/platform_manifest_twrp.git -b twrp-5.1

Then to sync up:

    repo sync

Then to build:

     cd <source-dir>; . build/envsetup.sh; brunch <device_name>
