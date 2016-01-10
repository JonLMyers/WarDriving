# Wardriving
Objective: Inform the Amherst community about the dangers of using outdated Wi-Fi encryption techniques.

# What is Wardriving?
Wardriving is the act of searching for and often mapping wireless network access points with a mobile device while driving in a vehicle. These access points are what your wireless device connects to when seeking to gain access to the internet and your network.  Once connected, you device will send information to this access point over Wi-Fi signals.  Unfortunately anyone who desires can easily observe this traffic without any special equipment or having access to your network.  This means that anyone could reconstruct your network traffic and view all the information you are sending over Wi-Fi if your traffic is not properly encrypted.  Malicious wardrivers take advantage of this by scouting out and mapping entire neighborhoods looking for vulnerable networks to prey on.  Once they have a selection of networks they can access them and perform actions such as stealing personal and private information or distributing child pornography.

This wardriving project and my personal intentions varied greatly from those that are held by malicious wardrivers.  Rather than mapping networks for future criminal activity, I gathered data to see how many home and small business wireless networks were not using encryption or still using WEP (Wired Equivalent Privacy - An encryption method that is outdated and ineffective).  I also refused to connect to anyone's private wireless network because connecting to non-public networks without permission is illegal.  

# The Fault in my WEP?
Non-Technical Summary: WEP is a terrible protocol for encryption and should not be used as it is easily crackable.

WEP (Wired Equivalent Privacy) was introduced with the original release of the 802.11 networking standard.  In the beginning WEP used both a 64 and 128 bit key for encryption.  Standard 64 bit WEP utilises the concatenation of a 24 bit initialization vector and a 40 bit key to form the complete key.  This 24 bit initialization vector was the downfall of WEP and is found in all of its versions.  In 2001 cryptographers discovered that the initialization vector was considered strongly non random due to the fact that 24 bits were not enough to prevent repetition on a network.  If someone was to process enough traffic on a network they could determine the key for the entire network and have unlimited access to all traffic.  This process is now easily automated and free software which has the capabilities of recovering the key in mere minutes is available to everyone. 

# Equipment Used
Hardware:
  Globalsat ‑ BU‑353S4 ‑ GPS receiver module
  TP-LINK TL-WN722N Wireless N150 High Gain USB Adapter
  Dell Inspiron Laptop with linux OS.
  
Software:
  Kismet - https://www.kismetwireless.net/
  Aciid's python script - https://github.com/Aciid/misc/blob/master/netxml2kml.py

Process: 
  The setup consited of installing all of the software and drivers for the peripherals and altering kismet's configuration file to      allow the network adapter/GPS.  After this setup was complete I simply drove around Amherst while kismet gathered and stored the GPS   coordinates of each individual network.  After two sessions of this I utilised Aciid's python script to turn the data into files      that can be opened and examined through Google Earth.
# Data
This image contains all of the networks using WEP as of 11/25/2015
![promisechains](https://cloud.githubusercontent.com/assets/14082284/12220051/91a6cf1a-b72b-11e5-8257-871cff9f63de.jpg)

This image contains all of the previous networks and newly explored areas as of 12/20/2015
![promisechains](https://cloud.githubusercontent.com/assets/14082284/12220052/93a39258-b72b-11e5-92e9-9162fb3d0c99.jpg)

# How to upgrade to WPA2 
