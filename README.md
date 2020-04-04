# Dns Safety for IOS
Dns Safety for Apple IOS is on-device DNS filter implemented as Network Extension. It can filter and block DNS requests from any application on your iPhone/iPad. This network extension can be used to block domains by name or site category. It also allows you to see what DNS requests were issued by installed applications.


## Limitations
According to Apple's documents DNS proxy implemented as Network Extension can only be run on a supervised (managed) device. To make your device managed you either use Apple Configurator 2 or some third party MDM solution. Although the setup is relatively simple, it does erase the iPhone (you can restore phone settings from the Apple Cloud backup afterwards).

See the following article on how to switch the Phone to supervised mode https://www.howtogeek.com/252286/how-to-put-an-iphone-or-ipad-into-supervised-mode-to-unlock-powerful-management-features/

## Pre installation requirements

In order to install the application you would need to generate a management profile for your device using Apple Configurator. A management profile is actually a file with .mobileconfig extension that is installed on the device using Apple Configurator. The following screenshots show steps required to create a new mobile config profile in Apple Configurator.

![Alt text](step1_new_profile.png?raw=true "New Profile") 

![Alt text](step2_general.png?raw=true "General Settings") 

![Alt text](step3_configure_dnsproxy.png?raw=true "Configure DNS Proxy Identifiers") 

To be sure the profile is installed correctly we also configure the lock screen message.

![Alt text](step4_lock_screen_message.png?raw=true "Lock Screen Message") 

Now save the profile into *DnsSafety.mobileconfig* file (download the configured [DnsSafety.mobileconfig](DnsSafety.mobileconfig) if needed).

![Alt text](step5_save_profile.png?raw=true "Save Profile as DnsSafety.mobileconfig file") 

The installed profile will be shown in the list of profiles on the device.

![Alt text](step6_view_profile.png?raw=true "View Installed Profile") 

Note, if needed you can simply download the profile from [DnsSafety.mobileconfig](DnsSafety.mobileconfig) and add it into the Application Configurator (i.e. do not use New Profile but Add Profile menu item). Adjust the profile settings as required (but do not change the app id of the network extension).

## How to install the application

Currently we distribute the application as AdHoc builds - this requires that the ID of your iPhone is built into the installer package. To do that please tell your device id to support@diladele.com - we will add it do the device list in the application package and send you the link to the package to install.
