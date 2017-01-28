Local manifests to build CyanogenMod/LineageOS 13 for [Chuwi Vi10 Plus](http://konstakang.com/devices/chuwi_vi10plus/CM13) and [Cube iWork8 Ultimate](http://konstakang.com/devices/cube_iwork8ultimate/CM13).

How to build:
-------------

Initialize repo:

    repo init -u git://github.com/LineageOS/android.git -b cm-13.0
    curl --create-dirs -L -o .repo/local_manifests/manifest_intel_cherrytrail.xml -O -L https://raw.githubusercontent.com/CM-CHT/android_local_manifest/cm-13.0/manifest_intel_cherrytrail.xml
    repo sync

### Chuwi Vi10 Plus:

    curl -L -o .repo/local_manifests/manifest_intel_chuwi_vi10plus.xml -O -L https://raw.githubusercontent.com/CM-CHT/android_local_manifest/cm-13.0/manifest_intel_chuwi_vi10plus.xml
    repo sync

Download and install poky toolchain to its default location (/opt/poky/1.8):

    wget http://downloads.yoctoproject.org/releases/yocto/yocto-1.8/toolchain/x86_64/poky-glibc-x86_64-core-image-sato-core2-64-toolchain-1.8.sh
    sudo ./poky-glibc-x86_64-core-image-sato-core2-64-toolchain-1.8.sh

Compile:

    . build/envsetup.sh
    brunch chuwi_vi10plus

### Cube iWork8 Ultimate:

    curl -L -o .repo/local_manifests/manifest_intel_cube_iwork8ultimate.xml -O -L https://raw.githubusercontent.com/CM-CHT/android_local_manifest/cm-13.0/manifest_intel_cube_iwork8ultimate.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch cube_iwork8ultimate
