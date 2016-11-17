Local manifests to build CyanogenMod 13 for [Chuwi Vi10 Plus](http://www.modaco.com/forums/topic/378038-cyanogenmod-13/) and [Cube iWork8 Ultimate](http://www.modaco.com/forums/topic/378037-cyanogenmod-13/).

How to build:
-------------

Initialize repo:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0
    curl --create-dirs -L -o .repo/local_manifests/manifest_intel_cherrytrail.xml -O -L https://raw.githubusercontent.com/CM-CHT/android_local_manifest/cm-13.0/manifest_intel_cherrytrail.xml
    repo sync

### Chuwi Vi10 Plus:

    curl -L -o .repo/local_manifests/manifest_intel_chuwi_vi10plus.xml -O -L https://raw.githubusercontent.com/CM-CHT/android_local_manifest/cm-13.0/manifest_intel_chuwi_vi10plus.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch chuwi_vi10plus

### Cube iWork8 Ultimate:

    curl -L -o .repo/local_manifests/manifest_intel_cube_iwork8ultimate.xml -O -L https://raw.githubusercontent.com/CM-CHT/android_local_manifest/cm-13.0/manifest_intel_cube_iwork8ultimate.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch cube_iwork8ultimate
