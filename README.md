
# What is this?

this repository containing the original boot.img of the latest HyperOS version (**OS1.0.5.0.UHZMIXM**) of the Xiaomi Redmi Note 12S (Global). and the OtrangeFox and TWRP usable for this same phone.

# How to flash OrangeFox on Redmi Note 12S:

Of course, you must already have the bootloader unlocked on your phone, and have the necessary drivers to recognize it in Fastboot mode, right? ok.

Download `orangeFox.img` from this repository, and also `bootOriginal.img`

Why download the `bootOriginal.img`? because we need it after flashing the recovery, put that file to the SD of your phone, preferably in a specific folder for your convenience.

Enter FastBoot mode

using [Platform Tools](https://developer.android.com/tools/releases/platform-tools?hl=es-419), open a terminal inside that folder, enter this command **(HEY, THIS WILL OVERWRITE YOUR BOOT.IMG ON YOUR PHONE)**:

```cmd
fastboot flash boot theRecoveryImage.img
```
If you receive this error (or similar):

![](https://github.com/Slushi-Github/Redmi_Note_12S_Assets/blob/main/readme/ErrorOnFlash.png)

Try with another cable!

If it was the opposite, your phone will reboot, you are already in OrangeFox recovery!
but... you don't have access to your HyperOS, because we overwrote the boot partition, relax, here is the next step:

Find the bootOriginal.img that you saved on your SD, and flash that bootOriginal.img to your boot partition, **BUT, DO NOT RESET**, you should still be in OrangeFox recovery, which is loaded in your memory.

