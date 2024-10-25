Instructions borrowed from Dennis Benders.

--------------
Install Ubuntu
--------------
1. https://rufus.ie/en/
2. https://medium.com/linuxforeveryone/how-to-install-ubuntu-20-04-and-dual-boot-alongside-windows-10-323a85271a73
3. https://ostoday.org/linux/best-answer-do-i-need-a-swap-partition-ubuntu.html
4. https://askubuntu.com/a/1264577/1530734
5. https://linuxize.com/post/how-to-add-swap-space-on-ubuntu-20-04/
6. https://help.ubuntu.com/community/SwapFaq
7. https://linuxconfig.org/how-to-install-ubuntu-20-04-alongside-windows-10-dual-boot


Notes:
- Create bootable USB using Rufus (1st link; do ony click on necessary buttons, e.g. not on cross for removing add after downloading).
- In case your laptop's drive is encrypted, turn it of (BitLocker) in Windows. This encryption is active if you have a laptop provided by the TU Delft. You might need to connect your power cable.
- In case you struggle with secure boot (e.g. cannot boot from USB stick), disable it in the bios
- Just create one partition for the root (see 2nd link, no swap and home partitions, see 3rd link).
- In case of memory shortage: check System monitor and/or /swapfile to check amount of swap space and increase if necessary (see links 4-6).
- For installing useful programs and settings, take a look at the suggested articles at the bottom of the 4th link.
- To check if you have UEFI boot, change the Bitlocker to off or check/add partitions, you need to be logged in with your .\localadmin account if you have a TU Delft laptop.
- Another useful website, is this one: https://itsfoss.com/install-ubuntu-1404-dual-boot-mode-windows-8-81-uefi/ (Used by Saray Bakker in Jan 2023)

--------------
Black screen after login with ubuntu (22.04):
--------------
- If it occurs that you can login, but after entering the password, your screen turns black, it might be a problem with your graphics drivers.
- You can still access ubuntu by doing a secure boot: When starting the laptop do: Advanced options, secure boot.
- To fix this issue, I used the following command in the terminal of ubuntu (from the secure boot): sudo ubuntu-drivers autoinstall
- and then rebooted my laptop (without secure boot). 
- I found this information on the website: https://www.linuxbabe.com/ubuntu/install-nvidia-driver-ubuntu
- After this you can go to: Software & Updates -> Additional Drivers.
- For me it now showed that my driver is Nvidia-driver-535 insteadof X.Org X server--Nouveau display driver. 
- If you install CUDA, you might need to again do a sudo ubuntu-drivers autoinstall and then reboot (also if it doesn't do it itself).
