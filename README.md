# Wardriving
**Objective: Inform the Amherst community about the dangers of using outdated Wi-Fi encryption techniques.**

Table of Contents:

- What is Wardriving?

- The Fault in my WEP?

- Equipment Used

- Data Examples

- How to Upgrade Your Encryption Method

# What is Wardriving?
Wardriving is the act of searching for and often mapping wireless network access points with a mobile device while driving in a vehicle. These access points are what your wireless device connects to when seeking to gain access to the internet and your network.  Once connected, you device will send information to this access point over Wi-Fi signals.  Unfortunately anyone who desires can easily observe this traffic without any special equipment or having access to your network.  This means that they could reconstruct your network traffic and view all the information you are sending over Wi-Fi if your traffic is not properly encrypted.  Malicious wardrivers take advantage of this by scouting out and mapping entire neighborhoods with vulnerable networks to prey on.  Once they have a selection of networks, they can access them and perform horresndous actions such as stealing personal and private information or distributing child pornography.

This wardriving project and my personal intentions varied greatly from those that are held by malicious wardrivers.  Rather than mapping networks for future criminal activity, I gathered data to see how many home and small business wireless networks were not using encryption or still using WEP (Wired Equivalent Privacy - An encryption method that is outdated and ineffective).  I also refused to connect to anyone's private wireless network because connecting to non-public networks without permission is illegal.  

# The Fault in my WEP?
**Non-Technical Summary: WEP is a terrible protocol for encryption and should not be used as it is easily crackable.**

WEP (Wired Equivalent Privacy) was introduced with the original release of the 802.11 networking standard.  In the beginning WEP used both a 64 and 128 bit key for encryption.  Standard 64 bit WEP utilises the concatenation of a 24 bit initialization vector and a 40 bit key to form the complete key.  This 24 bit initialization vector was the downfall of WEP and is found in all of its versions.  In 2001 cryptographers discovered that the initialization vector was considered strongly non random due to the fact that 24 bits were not enough to prevent repetition on a network.  If someone was to process enough traffic on a network they could determine the key for the entire network and have unlimited access to all traffic.  This process is now easily automated and free software which is available to everyone and has the capabilities of recovering the key in mere minutes. 

# Equipment Used
**Hardware:**
  - Globalsat ‑ BU‑353S4 ‑ GPS receiver module
  - TP-LINK TL-WN722N Wireless N150 High Gain USB Adapter
  - Dell Inspiron Laptop with linux OS.
  
**Software:**
  - Kismet - https://www.kismetwireless.net/
  - Aciid's python script - https://github.com/Aciid/misc/blob/master/netxml2kml.py

**Process:** 

  The setup consisted of installing all of the software and drivers for the peripherals and altering kismet's configuration file to     allow the network adapter/GPS.  After this setup was complete I simply drove around Amherst while kismet gathered and stored the GPS   coordinates of each individual network.  After two sessions of this I utilised Aciid's python script to turn the data into files      that can be opened and examined through Google Earth.
  
# Data Examples
**This image contains all of the networks using WEP as of 11/25/2015**
![promisechains](https://cloud.githubusercontent.com/assets/14082284/12220052/93a39258-b72b-11e5-92e9-9162fb3d0c99.jpg)

**This image contains all of the previous networks and newly explored areas as of 12/20/2015**
![promisechains](https://cloud.githubusercontent.com/assets/14082284/12220051/91a6cf1a-b72b-11e5-8257-871cff9f63de.jpg)

**To view all of the data in depth, please download the provided .kml and .kmz files and open them with Google Earth.**

# How to Upgrade Your Encryption Method 

- Login to your router using a device that is directly wired to it. (Example: A laptop/desktop using an ethernet cord.) To get to the login page you need to type your routers default ip address(Typically 192.168.0.1 or 192.168.1.1) into your browser's search bar.

![promisechains](https://cloud.githubusercontent.com/assets/14082284/12223756/786954c8-b7ad-11e5-93fa-c0aa55d61232.png)

- Upon arriving on a login screen like the image below you must enter your router's login credentials.  Oftentimes these credentials are still set to default.  This is also a major security issue because anyone could easily log onto your router and change any setting they desire.  You can find your router's default credentials using this website: http://www.routerpasswords.com/
![promisechains](https://cloud.githubusercontent.com/assets/14082284/12223755/75f9b16a-b7ad-11e5-8b29-0a18539273df.png)

- You will then need to navigate around your router's settings until you find the option to change encryption/security levels.  This will most likely be under the basic or advanced settings of your wireless tab.
![promisechains](https://cloud.githubusercontent.com/assets/14082284/12223758/7cf4b384-b7ad-11e5-8cec-505a6cfe9e52.png)

- Once you have found this setting make sure that you change it from WEP to either WPA-PSK or WPA2-PSK if it is available.
Now is also a great time to change your router's login credentials if they are still set to default. 
![promisechains](https://cloud.githubusercontent.com/assets/14082284/12223757/7adac4da-b7ad-11e5-9f69-e9365560832b.png)
