# Project 404, A project that shouldn't have exist by the laws of the internet just like the Schrödinger's cat xD

<p align="center">
<img src="https://raw.githubusercontent.com/markakash/404_stuff/master/project404-darkbanner.jpg" >
</p>

Sync sources:

    $ repo init -u https://github.com/P-404/platform_manifest -b qemu --depth=1
    $ mkdir -p .repo/local_manifests
    $ wget https://raw.githubusercontent.com/MocaRafee/manifest-rom/p404-whyred/zenx.xml -O .repo/local_manifests/roomservice.xml
    $ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Building for Xiaomi Redmi Note 5 Pro AI (Whyred)
---------------

To build:

    $ export LC_ALL=C
    $ . build/envsetup.sh
    $ lunch p404_whyred-userdebug
    $ mka bacon -j4 (or ram/2)
