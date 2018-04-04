android_device_quanta_narnia
==============

TWRP device tree for the LeapFrog Epic (MT8127) using OmniROM sources. Image needs to be signed using MTK signtool for Linux in order to be flashed properly via SP Flash Tool.

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | 1.3GHz Quad-Core MT8127
GPU     | Mali-450MP
Memory  | 1GB RAM
Shipped Android Version | 4.4.2
Storage | 16GB
Display | 7" 1024 x 600 px
Camera  | 2MPx rear, 2MPx front

* Compilation

        # repo init -u https://github.com/omnirom/android.git -b android-6.0
        
        # repo sync
        
        # source ./build/envsetup.sh

        # lunch omni_narnia-eng

        # mka recoveryimage
        
If done correctly, you should end up with a recovery.img in `/out/product/quanta/narnia`.

Make sure to sign it using the MediaTek sign tool (https://github.com/ferhung-mtk/android_kernel_huawei_h30t00/tree/master/kernel-3.4/mediatek/build/tools/SignTool) prior to flashing. ;)

## Issues/Caveats
* Bootloader still needs some TLC. Not sure how to hack LK to provide proper fastboot support though.

## Todo
* Nothing?

## Downloads
You may download the initial recovery releases for the vanilla SE here: https://github.com/huckleberrypie/device_quanta_narnia/releases

## Special thanks
Major props to neporood for the friendship and advice, Kevin Giles, diplomatic@XDA for being the ultimate MTK fanboi and schooling yours truly about the inner workings of MediaTek devices, my pals at the American Girl collectors groups (Molly, Shannon, Amy...), and to everyone else worth thanking. ;)
