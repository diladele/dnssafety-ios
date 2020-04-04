# Dns Safety for IOS
Dns Safety for Apple IOS is on-device DNS filter implemented as Network Extension. It can filter and block DNS requests from any application on your iPhone/iPad. This network extension can be used to block domains by name or site category. It also allows you to see what DNS requests were issued by installed applications.


## Limitations
According to Apple's documents DNS proxy implemented as Network Extension can only be run on a supervised (managed) device. To make your device managed you either use Apple Configurator 2 or some third party MDM solution. Although the setup is relatively simple, it does erase the iPhone (you can restore phone settings from the Apple Cloud backup afterwards).

See the following article on how to switch the Phone to supervised mode https://www.howtogeek.com/252286/how-to-put-an-iphone-or-ipad-into-supervised-mode-to-unlock-powerful-management-features/
