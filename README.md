# Nameless-AOSP-Opensource #

How to build Nameless-AOSP for your device - Tutorial
==============================================

Downloading Nameless-AOSP-Opensource Source Codes
-------------------------------

To get started with the building process, you'll need to get familiar with [Git and Repo](http://source.android.com/source/using-repo.html).


# Initialize local repository
```bash
repo init -u https://github.com/NAMELESS-AOSP-OPENSOURCE/manifest.git -b nameless
```
To save time, space and internet data during sync, use a command like this:

```bash
repo init -u https://github.com/NAMELESS-AOSP-OPENSOURCE/manifest.git -b nameless --depth=1
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
