# OdroidGoWIFIHASHMONSTER
Instructions on how to get the ESP32 Wifi Hashmonster working on the Odroid Go


Installing The Wifi Hashmonster on an Odroid Go

Required Software: Arduino IDE 
Required Hardware: Odroid GO and up to 32GB micro SD card to store PCAP files.
Required libraries: 
https://github.com/G4lile0/ESP32-WiFi-Hash-Monster - MAIN CODE REPO
https://github.com/tobozo/ESP32-Chimera-Core
https://github.com/lovyan03/LovyanGFX
https://github.com/tobozo/M5Stack-SD-Updater
https://github.com/hardkernel/ODROID-GO.git

Controls: 
A button: short press =switches to incognito mode: Blanks out the screen.
A button: Long press = Turns off/on the sd card.
Menu Button: Short press = switches channel
Menu Button: Long press = sets to Channel Fixed Mode from Automatic switching.

Install the ODROID-GO library by either downloading the repository or executing commands 

Windows: 
git clone https://github.com/hardkernel/ODROID-GO.git $USERPROFILE/Documents/Arduino/libraries/ODROID-GO

Linux:
git clone https://github.com/hardkernel/ODROID-GO.git ~/Arduino/libraries/ODROID-GO

MacOS:
git clone https://github.com/hardkernel/ODROID-GO.git ~/Documents/Arduino/libraries/ODROID-GO

You need to select the Ordoid ESP32 to upload the wifi hashmonster code
Select Tools → Board → ODROID ESP32.
Select the proper COM port. If your ESP32 is not detecting on a COM port You may need this driver https://www.silabs.com/developers/usb-to-uart-bridge-vcp-drivers?tab=downloads
Open the .INO file from the ESP32-WiFI-Hash-Monster
Ctrl-F to find this line <#define MAX_SSIDS> Change this number to 1750 to avoid memory overflow errors.
Run verify to make sure the code compiles correctly.
If it compiles you should be good to go. Go ahead and switch on the Odroid-GO and hit upload.
