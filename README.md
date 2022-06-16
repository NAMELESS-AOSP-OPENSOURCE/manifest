# Nameless-AOSP #

How to build Nameless-AOSP for your device - Tutorial
==============================================

Downloading Nameless-AOSP Source Codes
-------------------------------

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).


# Initialize local repository
```bash
repo init -u git@github.com:Nameless-AOSP/manifest.git -b twelve
```
To save time, space and internet data during sync, use a command like this:

```bash
repo init --depth=1 -u git@github.com:Nameless-AOSP/manifest.git -b twelve
```
# Sync
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

# Build

# Set up environment
```bash
$ . build/envsetup.sh
```
# Choose a target
```bash
$ lunch aosp_$device-userdebug
```
# Build the code
```bash
$ mka bacon -jX
```
