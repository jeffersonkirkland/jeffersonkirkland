---
layout: post
title: "Booting A Chromebook From USB"
categories: chromebook,linux
author:
- Jefferson Kirkland
---

# Intro

First, a little backstory into why this post...

I have an older, low-end Chromebook that has been sitting around gathering dust. Sure, I could probably put it on Facebook Marketplace and find a good home for it.... but the specs, ugh!!  

I turned it on, and logged into it to take a look around.  I was thinking about re-installing it with a distribution of Linux for systems with older or lower system specs, but I didn't realize how low they were.  Dual cpu, fine. Ram only had 2gb. To be honest, that isn't reasonable even for most of the low resource linux distributions out there.  Then the storage space was only 2gb.  Great for ChromeOS, as it allows you to store your files on Google drive, but not for standard linux.  With those low ram specs, getting the desktop running wouldn't be a fun endeavor.  

I was going to use this as a computer for coding projects for the Arduino, but I have other laptops that can do the trick.  This thing just isn't going to cut it and will probalby just donate it to Savers or something.  

Anywho, the reason for this posting was to let you know how you can boot your Chromebook from a USB drive, in order to install another operating system (like Linux).  So, I am going to, at least, provide you those details.  


# The Nitty Gritty

## Turning OFF OS Verification

Ok, so first thing you need to do is have a Chromebook and be logged into it.  At the desktop, hit ESC+REFRESH+POWER.  This will put you into recovery mode, which is where you want to be.  Now, you need to turn off OS Verification (ChromeOS likes to always verify that you are ONLY using ChromeOS).  Hit CRTL+D and then hit ENTER.

Let the machine work, even though it doesn't look like its doing anything.  It will reboot once.  Once it is done, it will be at the **OS Verification** screen.  At this point, you can either wait for 30 seconds, or hit **CTRL-D** to continue to the OS.  You will have to go through setup again. 


## Setup To Boot From USB

Now you need to enable support for booting from USB.  Once you are back at the desktop, you will hit **CRTL+ALT+F2** (F2 will be the right arrow in the top row (->)) to bring up the console window.  You will now do the following:

1. At the prompt for login enter **chronos** and hit **ENTER**
2. Type **sudo bash** and hit **ENTER**
3. Type **crossystem dev_boot_usb=1 dev_boot_legacy=1** and hit **ENTER**
(You may get an error about the **dev_boot_legacy** portion and will instead need to use **dev_boot_altfw**.  If so, do it again and use that instead, as instructed.
4. Type **sudo reboot**

Now, the system will reboot and will come back up and put you again at the **OS Verification** screen.  Hit **CTRL+L** to bring you to the legacy bios screen, where you can select your boot device.  Here you will choose the usb drive (assuming you have the usb drive with your alternate OS already inserted). 

# Wrapping It Up

Hopefully that works for you.  I wish the Chromebook I have/had contained better spects, but that's neithere here nor there.  I have other machines.  If you have one with better specs, I hope this helps you reclaim the machine from ChromeOS and give it more functionality. 



