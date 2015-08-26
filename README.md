Zedroid -Android 5.0 and later on Zedboard(Zynq-7000)-

See this manual -How to Use(Build) this project- :
https://www.slideshare.net/noritsuna/zedroid-android-50-and-later-on-zedboard/

How to Use This Binary:
1, Make partitin on your SD Card:
1st partition as primary: VFAT(FAT32) with boot flag over 100MB
2nd partition as primary: ext4 over 1GB
3rd partition as primary: ext4 over 500MB
4th partition as primary: Linux Swap over 512MB

2, Download files:
boot.bin
devicetree.dtb
uImage
uramdisk.image.gz
system_dir-GLES12.tar.xz.??

3, Copy files as boot:
sudo cp boot.bin [sd card 1st partition]
sudo cp devicetree.dtb [sd card 1st partition]
sudo cp uImage [sd card 1st partition]
sudo cp uramdisk.image.gz [sd card 1st partition]

4, Copy files as Android System:
copy system_dir-GLES12.tar.xz.?? system_dir-GLES12.tar.xz
sudo tar Jxfv system_dir-GLES12.tar.xz
sudo cp -aR system/* [sd card 2nd partition]/

5, Try to boot!

