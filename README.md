# Pixel Experience Fans Edition

<p align="center">
<img src="https://avatars2.githubusercontent.com/u/62373445?s=200&v=4" >
</p>

Sync sources:
    $ repo init -u https://github.com/MocaRafee/manifest-pe -b ten-fe  --depth=1
    $ mkdir -p .repo/local_manifests
    $ wget https://raw.githubusercontent.com/MocaRafee/manifest-rom/pe10_fe/pekenzo.xml -O .repo/local_manifests/roomservice.xml
    $ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Building for Xiaomi Redmi Note 3 (kenzo/kate)
---------------

To build:

    $ export LC_ALL=C
    $ . build/envsetup.sh
    $ lunch aosp_kenzo-userdebug
    $ mka bacon -j$(nproc --all)
