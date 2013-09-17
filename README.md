evga-8400-gs
============

Files and info to get an EVGA GeForce 8400 GS 512MB graphics card working in a hackintosh 10.6.8

I had an ASUS version of this same card fully working in another set up so thought that this one would also work with the graphics enabler kext but not so. Only got the basic 1024x768 on my 1920x1200 monitor. Took more or less a whole weekend of tinkering and finally got it but by accident it seems :)

It's in a quad core Dell optiplex 755 with the Mac OS set up using iBoot and Multibeast with a retail Snow Leopard. Current state of kexts and plist files as follows.

All geforce kexts and NV kexts deleted. Then installed the Quadro drivers from Nvdia's site. The Hal100 and Hal50 kexts have been edited to include the device ID. The resman kext also has this. I tried adding an EFI string to my org.chameleon.boot.plist but made everything go back to zero. This I commented out. I tried NVEnabler64.kext (also with the Device ID) but didn't do much. This was in /Extra/Extensions. I managed to get 1600x1200 for a time but got a blue screen when I tried to change the resolution. Finally, I deleted the NVEnabler64.kext and reinstalled it - boom. It worked! Full resolution.
