Currently supported platform under validations:

Atom:

    Intel Joule 570x
    APL-NUC [NUC6CAYH]

Core:

    KBL-NUC [NUC7i5BNH-IDD]

More open platforms are being added.
Downloading the source code

The source code is managed with same repo tool chain as Google AOSP (Android Open Source Project).
Getting the repo script

curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo

chmod a+x ~/bin/repo
Using https protocols:

mkdir trusty-ia

cd trusty-ia

repo init -u https://github.com/trusty-ia/manifest

or you can specify the branch:

repo init -u https://github.com/trusty-ia/manifest -b omr1
Sync Code

repo sync -j5
Building the image

make

or enable the parallel making

make -j5

You will find the built binaries in out folder.

out/ikgt is the home folder for hypervisor and out/trusty is the home folder for trusty os.
Flashing

Currently trusty bundle (ikgt hypervisor and trusty os) requires the integration with Android to make it functional. A reference AOSP code base with Trusty support is available based on Intel open source Android project Celadon.
Android support

Trusty-IA supports Android for x86 in Celadon project. https://github.com/projectceladon/manifest/wiki
