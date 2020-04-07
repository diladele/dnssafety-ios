# Dns Safety for iOS
Dns Safety for Apple iOS is on-device DNS filter implemented as Network Extension. It can filter and block DNS requests from any application on your iPhone/iPad. This network extension can be used to block domains by name or site category. It also allows you to see what DNS requests were issued by installed applications.


## Limitation 1 - Your iPhone must be supervised

According to Apple's documents DNS proxy implemented as Network Extension can only be run on a supervised (managed) device. To make your device managed you either use Apple Configurator 2 or some third party MDM solution. Although the setup is relatively simple, it does erase the iPhone (you can restore phone settings from the Apple Cloud backup afterwards).

See the following article on how to switch the Phone to supervised mode https://www.howtogeek.com/252286/how-to-put-an-iphone-or-ipad-into-supervised-mode-to-unlock-powerful-management-features/

## Limitation 2 - You need to add management profile allowing Dns Proxing

In order to install the application you would need to generate a management profile for your device using Apple Configurator. A management profile is actually a file with .mobileconfig extension that is installed on the device using Apple Configurator. The following screenshots show steps required to create a new mobile config profile in Apple Configurator.

![Alt text](step2_general.png?raw=true "General Settings") 

![Alt text](step3_configure_dnsproxy.png?raw=true "Configure DNS Proxy Identifiers") 

To be sure the profile is installed correctly we also configure the lock screen message.

![Alt text](step4_lock_screen_message.png?raw=true "Lock Screen Message") 

Now save the profile into *DnsSafety.mobileconfig* file (download the configured [DnsSafety.mobileconfig](DnsSafety.mobileconfig) if needed).

![Alt text](step5_save_profile.png?raw=true "Save Profile as DnsSafety.mobileconfig file") 

The installed profile will be shown in the list of profiles on the device.

![Alt text](step6_view_profile.png?raw=true "View Installed Profile") 

Note, if needed you can simply download the profile from [DnsSafety.mobileconfig](DnsSafety.mobileconfig) and add it into the Application Configurator (i.e. do not use New Profile but Add Profile menu item). Adjust the profile settings as required (but do not change the app id of the network extension).

## Limitation 3 - You need to use Test Flight

The application is in beta stage and was recently approved by Apple to be distributed using Test Flight. So if you would like to participate, just send a request to support@diladele.com and we will add your e-mail to the Test Flight beta list. Apple will then send you the invitation link and you can install the application.

## How to use the application

Currently the application is very basic but it proves the ability to filter DNS requests on iPhone. It is possible to block any DNS request by domain name and also block well known advertisement networks. The same settings work in Wi-Fi and 4G/LTE network connections. Internally DNS requests are forwarded to 8.8.8.8 so if using within your Wi-Fi network make sure you are not blocking access to it.

## Support

Please direct your support requests to support@diladele.com or write at the forum at https://groups.google.com/forum/#!forum/web-safety. Issues and ideas can be supplied directly in this repo of course.

