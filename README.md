# LiquidRemix Pie

Synch sources:

    $ repo init -u https://github.com/Bootleggers-BrokenLab/manifest.git -b queso
    $ mkdir -p .repo/local_manifests
    $ wget https://raw.githubusercontent.com/magicxavi/manifest/BootleggersROM/BootleggersROM.xml -O .repo/local_manifests/roomservice.xml
    $ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Building for Xiaomi Redmi Note 3 (kenzo/kate)
---------------

To build:

    $ export LC_ALL=C
    $ . build/envsetup.sh
    $ lunch bootleg_kenzo-userdebug
    $ mka bacon -j36
