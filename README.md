Local manifests to build CyanogenMod 10.2 for [ZTE Blade](http://www.modaco.com/topic/365330-cyanogenmod-10.2/) and [ZTE Blade III](http://www.modaco.com/topic/364042-cyanogenmod-10.2/).

How to build:
-------------

Initialize repo:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-10.2
    curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-10.2/local_manifest.xml
    repo sync

### Blade:

    curl -L -o .repo/local_manifests/local_manifest_armv6.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-10.2/local_manifest_armv6.xml
    curl -L -o .repo/local_manifests/manifest_zte_blade.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-10.2/manifest_zte_blade.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch blade

### Blade III:

    curl -L -o .repo/local_manifests/manifest_zte_atlas40.xml -O -L https://raw.githubusercontent.com/legaCyMod/android_local_manifest/cm-10.2/manifest_zte_atlas40.xml
    repo sync

Compile:

    . build/envsetup.sh
    brunch atlas40

