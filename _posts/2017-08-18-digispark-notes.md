---
title: "Digispark Notes"
date: "2017-08-18"
categories: 
  - "hacking"
  - "programming"
---

 

http://handshake.co.za/2014/digispark-the-micro-sized-affordable-arduino-enabled-usb-development-board/ ++++++++++++++++++++++++++++++++++++++++++++++++++++

SYSTEM: Windows 8.1 x64

PROBLEM 1: You try to program the Olimexino-85 (or Digispark device, or whatever brought you to this page), and a Windows error message pops up: “USB device not recognized” then something like “The last USB device you connected to this computer malfunctioned, and Windows does not recognize it.”

TROUBLESHOOTING 1: 1) Re-install the latest Arduino IDE (now it’s 1.6.11) 2) Download the Digistump.Drivers.zip again (now it’s 1.6.7) from: https://github.com/digistump/DigistumpArduino/releases/download/1.6.7/Digistump.Drivers.zip 3) Unzip this drivers file and run the InstallDrivers.exe Wizard.

PROBLEM 2: The drivers finish installing but the Ports driver has failed:

Install failed: Digistump LLC (usbser) Ports (08/16/2014 1.1.0.0) Ready to use: libusb-win32 Digispark Bootloader (01/17/2012 1.2.6.0) Ready to use: libusb-win32 DigiUSB (09/02/2014 1.2.6.1) Ready to use: Digistump LLC (digistump.com) (usber) Ports (09/02/2014 5.1.2600.1)

TROUBLESHOOTING 2: Just plug in the little Olimexino-85 or Digispark device to a USB port. It might give the Problem 1 again but ignore it for now. 1) Go into Device Manager, under Universal Serial Bus Controllers, look for item with the yellow caution “!” next to it. It’s probably called: Unknown USB Device (Device Descriptor Request failed) 2) Right click on it, then click on Properties.

PROBLEM 3: The device status has an error message in it, like this:

Windows has stopped this device because it has reported problems. (Code 43) A request for the USB device descriptor failed.

TROUBLESHOOTING 3: Try updating the driver. 1) Go to the tab for Drivers and click Update Driver.

But what do we do if it says: The best driver software for your device is already installed. Windows has determined the driver software for your device is up to date. ??

TROUBLESHOOTING 4: Try checking the file called DigiSerial.inf, maybe it’s missing the usbser.sys line.

1) Search computer for DigiSerial.inf, find it buried way, way, way in the depths of your User folders. 2) Open it in a WordPad or similar and find the line that say \[DriverInstall.NTamd64.CopyFiles\] 3) Check that both these files are listed underneath there: usbser.sys lowcdc.sys

But what do we do if they’re already there??

DIAGNOSIS OF PROBLEM: Seems like we need to fix the initial Ports installation failure. This is the magical answer that many people have been asking for over the past few months…

Please help!

 

 

 

 

 

 

 

 

 

\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_

 

 

 

OK — good news. If you read my post from Sept 9th and are still frustrated that your Olimexino-85 isn’t being read as a device by Windows, I’ve finally got mine working. I had to manually install a special driver, and I used a small program called “Zadig” to do it for me. This process fixes the initial Ports installation failure, and after doing the following steps, I successfully programmed my Olimexino-85 with a little blink program. I will only add that I did not have to re-program the bootloader that came with it, which was a suggestion that came straight from support (at) olimex.com. (Their other final suggestion was to check the soldering around the USB socket.)

If you have Windows Vista or later: (includes Windows 8 & 10) 1) Create a folder on the Desktop called “Zadig” or similar. 2) Open an empty Notepad file. 3) In Firefox, go to https://github.com/micronucleus/micronucleus/tree/master/windows\_driver\_installer 4) Right-click the zadig\_2.1.2.exe file link and save it to your folder. Check in Windows Explorer: If the filename has changed to “.htm” for internet protection, rename the file back to just “.exe”. 5) Left-click on the Zadig.ini file link to go in and see its contents (31 lines). Copy & paste the entire text into a new Notepad file and save it with the .ini extension, in your Zadig folder. 6) Go back to the weblink in step 3 (go up one level). 7) Left-click on the micronucleus.cfg file link to go in and see its contents (8 lines). Copy & paste the text into a new Notepad file, and save it with the .cfg extension, in your Zadig folder. 8) In Windows Explorer, look in the Zadig folder and confirm you have these 3 files: – Zadig.ini – micronucleus.cfg – zadig\_2.1.2.exe 9) Connect the Olimexino-85 board to a USB port on your computer. Close the pop-up window if it tries to install a driver by itself. 10) Run the zadig\_2.1.2.exe application. If necessary, allow the program to make changes to your computer. (The verified publisher is Akeo Consulting.) 11) In Zadig, click: Device > Load Preset Device, and select the micronucleus.cfg in your Zadig folder. You should see “Micronucleus” written inside the text box. 12) Next to the green arrow, change the WinUSB selection to be the libusb-win32 selection. 13) Underneath the libusb-win32 text box is the installation button. Make sure to select “Install Driver” from the drop-down menu on the button, then click on the button to activate the installation. 14) You can check to see if the installation was successful: in Zadig, click Options > List All Devices. Look for the “Digispark bootloader” option.

I hope this works for you too. 🙂
