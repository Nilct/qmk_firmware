# 

Built from : The default keymap for xd75, with led controls with `~/dev/keyboard/qmk_firmware/util$ ./new_keymap.sh xd75 nil_ct_preoniclike`

Instructions :

```
Compile a firmware file with your new keymap by typing: 
   make xd75:nil_ct_preoniclike
from the qmk_firmware directory
```

## Inspiration

The goal is to have a similar layout as Preonic. The left part of the keyboard is the same.


## Flash

```
clear; make xd75:nil_ct_preoniclike:flash
...
dfu-programmer: no device present.
ERROR: Bootloader not found. Trying again in 5s.
```

```
(base) nil@arthur:~/dev/keyboard/qmk_firmware$ lsusb -v
Bus 001 Device 008: ID 03eb:2ff4 Atmel Corp. atmega32u4 DFU bootloader
Couldn't open device, some information will be missing
Device Descriptor:
  bLength                18
  bDescriptorType         1
  bcdUSB               2.00
  bDeviceClass          255 Vendor Specific Class
  bDeviceSubClass         1 
  bDeviceProtocol         0 
  bMaxPacketSize0        32
  idVendor           0x03eb Atmel Corp.
  idProduct          0x2ff4 atmega32u4 DFU bootloader
  bcdDevice            0.00
  iManufacturer           1 
  iProduct                2 
  iSerial                 3 
  bNumConfigurations      1
  Configuration Descriptor:
    bLength                 9
    bDescriptorType         2
    wTotalLength           18
    bNumInterfaces          1
    bConfigurationValue     1
    iConfiguration          0 
    bmAttributes         0x80
      (Bus Powered)
    MaxPower              100mA
    Interface Descriptor:
      bLength                 9
      bDescriptorType         4
      bInterfaceNumber        0
      bAlternateSetting       0
      bNumEndpoints           0
      bInterfaceClass         0 (Defined at Interface level)
      bInterfaceSubClass      0 
      bInterfaceProtocol      0 
      iInterface              0 

```

dfu-util -l
