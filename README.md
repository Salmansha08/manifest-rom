# Zenx based on Android 10

<p align="center">
<img src="https://github.com/ZenX-OS/XDA/blob/master/Images/ZenX-OS_logo.png" >
</p>

Sync sources:

    $ repo init -u https://github.com/RevengeOS/android_manifest -b r11.0 --depth=1
    $ mkdir -p .repo/local_manifests
    $ wget https://raw.githubusercontent.com/rio-31/manifest-rom/Revenge11/revengeos.xml -O .repo/local_manifests/roomservice.xml
    $ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Building for Xiaomi Redmi Note 3 (kenzo/kate)
---------------

To build:

    $ export LC_ALL=C
    $ . build/envsetup.sh
    $ lunch revengeos_kenzo-userdebug
    $ mka bacon -j12
