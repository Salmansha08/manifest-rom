# ExtendedUI #

<p align="center">
<a ="https://raw.githubusercontent.com/Extended-UI/android_manifest/android_10/ExtendedUI-banner.jpg">
</p>

Sync sources:

    $ repo init -u https://github.com/rio-31/extendedUI_manifests.git -b android_10
	or shallow clone if you don't have much bandwith
    $ repo init -u https://github.com/rio-31/extendedUI_manifests.git -b android_10  --depth=1
    $ mkdir -p .repo/local_manifests
    $ wget https://raw.githubusercontent.com/rio-31/manifest-rom/exUI/exui.xml -O .repo/local_manifests/roomservice.xml
    $ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Building for Xiaomi Redmi Note 3 (kenzo/kate)
---------------

To build:

    $ export LC_ALL=C
    $ . build/envsetup.sh
    $ lunch aosp_kenzo-userdebug
    $ mka bacon -j$(nproc --all)
