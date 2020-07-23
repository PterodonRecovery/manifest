## Getting Started ##
---------------

To get started with OMNI sources to build Pterodon Recovery, you'll need to get
familiar with [Git and Repo](https://source.android.com/source/using-repo.html).

To initialize your local repository using the OMNIROM trees to build Pterodon Recovery, use a command like this:

    repo init -u git://github.com/PterodonRecovery/manifest.git -b master

To initialize a shallow clone, which will save even more space, use a command like this:

    repo init --depth=1 -u git://github.com/PterodonRecovery/manifest.git -b master

Then to sync up:

    repo sync

Then to build for a device with recovery partition:

     cd <source-dir>; export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch omni_<device>-eng; mka recoveryimage

Then to build for a device without recovery partition:

     cd <source-dir>; export ALLOW_MISSING_DEPENDENCIES=true; . build/envsetup.sh; lunch omni_<device>-eng; mka bootimage
