# Komodo OS Rom #

<p align="center">
<a href="https://imgur.com/8RoBGQS"><img src="https://i.imgur.com/8RoBGQS.png" title="Banner"/></a>
</p>

Sync sources:

    $ repo init -u https://github.com/Komodo-OS-Rom/manifest.git -b ten
	or shallow clone if you don't have much bandwith
    $ repo init -u https://github.com/Komodo-OS-Rom/manifest.git -b ten  --depth=1
    $ mkdir -p .repo/local_manifests
    $ wget https://raw.githubusercontent.com/rio-31/manifest-rom/komodo10/komodo.xml -O .repo/local_manifests/roomservice.xml
    $ repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

Building for Xiaomi Redmi Note 3 (kenzo/kate)
---------------

To build:

    $ export LC_ALL=C
    $ . build/envsetup.sh
    $ lunch komodo_kenzo-userdebug
    $ masak komodo -j$(nproc --all)
