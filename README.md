# BT Smart Web

Demo controlling the fischertechnik BT smart controller via Web
Bluetooth and/or Web USB.

To run this demo open the following link using google chrome:
https://technika-karlsruhe.github.io/bt_smart_web/

This demo has been tested under Windows, Linux and Android.

## Linux

Under Ubuntu Linux the Chrome/Chromium is by default installed from
a snap archive and is by default sandboxed. It thus doesn't have
the necessary permissions to access USB. The following command
allows for raw USB access from within Chrome/Chromium:

```
sudo snap connect chromium:raw-usb
```

Furthermore direct USB permissions may need to be given to the current
user. Creating a file named ```/etc/udev/rules.d/99-btsmart.rules```
containing the following line will give the necessary permissions.

```
ATTRS{idVendor}=="221d" ATTRS{idProduct}=="0005", MODE="664", GROUP="plugdev"
```

## Android

The demo runs out of the box with the chrome preinstalled on any
recent android device. However, for the USB version to work a
so-called "USB to mini USB host mode cable" or "USB on-the-go (OTG) to
mini USB adapter" is needed. This cable should have a connector
matching your Android device on one side (e.g. USB-C on recent phones)
and a Mini-USB connector on the other side matching the BT Smart
controller.

![Android USB](android_usb.jpg)