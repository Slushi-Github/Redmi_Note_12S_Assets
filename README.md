
# What is this?

this repository containing the original boot.img of the latest HyperOS version (**OS1.0.5.0.UHZMIXM**) of the Xiaomi Redmi Note 12S (Global). and the OtrangeFox and TWRP usable (?) for this same phone.

Boot Image from: https://xiaomifirmwareupdater.com/hyperos/sea/stable/OS1.0.5.0.UHZMIXM/

OrangeFox Image from: https://github.com/shazu-xd/releases/releases/download/vofox/OrangeFox-R12.1_1-Stable-sea.img (The page not exist..)


This repository, I don't think I will update it constantly.

Also, I am not a contribution of the Xioami community or this specific phone, I just want to facilitate how to do certain steps from my own experience.

And as I am not the owner of the recoveries, possibly with HyperOS updates, or another problem, they will stop working and I will not do anything to fix that.

if you have any suggestions for this repository, I am happy to see them and take them into account if they are really worth it :3

This is my first repository made for the public, probably there are some mistakes, sorry hehe...

# How to flash OrangeFox on Redmi Note 12S:

I AM NOT RESPONSIBLE FOR ANY DAMAGE THAT MAY RESULT FROM THIS PROCEDURE EVEN IF IT IS APPLIED ON THE SAME DEVICE.

IF FOR SOME REASON YOU GET STUCK IN A BOOTLOOP AFTER FLASHING THE `orangeFox.img`, GO BACK TO FASTBOOT AND FLASH THE `bootOriginal.img`.

Of course, you must already have the bootloader unlocked on your phone, and have the necessary drivers in your PC to recognize it in Fastboot mode, right? ok.

Download `orangeFox.img` from this repository, and also `bootOriginal.img`

Why download the `bootOriginal.img`? because we need it after flashing the recovery, put that file to the SD of your phone, preferably in a specific folder for your convenience.

Enter FastBoot mode

using [Platform Tools](https://developer.android.com/tools/releases/platform-tools?hl=es-419), open a terminal inside that folder, enter this command **(HEY, THIS WILL OVERWRITE YOUR BOOT.IMG ON YOUR PHONE)**:

```cmd
fastboot flash boot theRecoveryImage.img
```
If you receive this:

![](https://github.com/Slushi-Github/Redmi_Note_12S_Assets/blob/main/readme/CorrectFlash.png)

Perfect, the flash is completed!
Your phone will reboot, if not, use this:

```cmd
fastboot reboot
```
After the reboot, you are already in OrangeFox recovery!
but... you don't have access to your HyperOS, because we overwrote the boot partition, relax, here is the next step:
Find the bootOriginal.img that you saved on your SD, and flash that bootOriginal.img to your boot partition, **BUT, DON'T RESET**, you should still be in OrangeFox recovery, which is loaded in your memory.
In the bottom bar, go to the last option, [Menu],

you should see an option called ``Flash current OrangeFox``, go to that option and use it, it will flash the OrangeFox you have in memory, in the original boot partition of your Redmi Note 12S.
Now you can reboot and get back to your HyperOS.

