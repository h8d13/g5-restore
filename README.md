# g5-restore

Checking for serials. 

You can find them under the main cover. I had bought 3 from FB marketplace (for 150$): 

Cl62901ev5w dual 2.3 512 250 6600 
G853758gru2 2.0 51 160 9600

So based on this we can already tell which one is useless and which one is good :)

Luckily from the 3 I bought 2 of them were the later 2.3 Ghz releases which use regular PCIe (versus AGP connectors) which means we can upgrade most pieces.

## Checking power cables & water damage
--- 

![1e4da476-6ee0-4aed-aafc-71de666b32878145070884849698766](https://github.com/user-attachments/assets/b7df1aa5-77a9-419b-b09e-df51c4f6f867)

So this is a C19-C20 cable for the later 2005 g5's.The cases are super heavy but also cool looking!

These can draw 30-50% more amps, while earlier versions use the common C13-C14 cables you find on many devices still to this day. 

The power supply on these is seated at the bottom and takes the full width of the base of the computer, it's a pretty crazy set-up but they can be found second hand or refurbished.It is also quite ez to retrofubrish a more modern PSU into the case. 

Better to check the cables for damage (often  present when they were plugged-in/out many times) and get new cables. I decided to get new ones cause mine looked like hell. 

## RAM
---

The original ram sticks are horrible for modern comparison, upgrade safely with backwards compatibility to:

240 Pin Dimm - 1.8v - PC2-4200 (533Mhz) - ECC Registered x4 2GiB

Bringing our ram from 512 mb (2x 256mb) to 8Gib. Which is considerable upgrade!

## Memory
---
We can use regular SATA SSDs which are backward compatible even tho we will not get the full speed, you can get them for cheap reconditionned (20$ for 512 GiB)

## GPU
---
You can also go wild and upgrade GPU using regular PCIe connectors, you can also get modifications boards with the remaining PCIe slots!

## SPECIAL THANKS
---
https://www.youtube.com/watch?v=cS58kQ10qas

Check Casey Cullen's channel out on YouTube!!!!!

## Booting
---

Hold command and option at the same time + O and F (OpenFirmware) 
You should now see a console like white terminal. 
If you're struggling to see this screen here are two tips:
  If you're using a regular keyboard its ALT and Windows key.
  If you're seeing the regular old OS directly i recommend removing the drive altogether. 

The video above explains nicely how to use:
```
dev / ls 
or
devalias 
```

You need to look for devices listed under UD, USB, DISK

Which helps to find all your devices (didn't want to burn a CD, it's not 2005 unfortunalty)

You can then boot from USB (I used the 3rd port down on back panel) 
``` boot usb3/disk@2:2;\\yaboot ``` 
Note:

Disk 2: partiton 2 is default

Getting started
---

Make sure to use a power pc compatible install: I used: https://cdimage.debian.org/cdimage/ports/12.0/powerpc/

Also make sure to plug the ethernet cable into the top port (port 0) as this will be used to make the full Debian install. 

I ignored most of the warnings for mirrors and minimal install, as I kind of knew it would be hell since I hadn't received the new RAM yet. 
Took 60 seconds for the first Init script to start...

And the mac pro g5 was screaming through half of the install. 


Attempt #2
---

So I thought let's try something else...

I used the ISO from the video:

https://fienixppc.blogspot.com/p/blog-page.html

Which is specifically designed to have a minimal Mate Desktop which would help a lot and many more base packages. 

Repeated the boot process and voilà. 






