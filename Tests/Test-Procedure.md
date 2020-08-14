ESP-Flasher Test Procedure
==========================

Open Simplicity Studio.

Select CP2102N as the device type.

Important settings:

 * Max Power (mA) = 500
 * Power Mode = Bus Powered
 * Port Drive Strength = High Drive
 * DTR: Reset Mode = Push-Pull
 * RTS: Reset Mode = Push-Pull
 * GPIO0: Reset Mode = Push-Pull, Alternate Function = TX Toggle
 * GPIO1: Reset Mode = Push-Pull, Alternate Function = RX Toggle

Plug in device using USB-C cable.

Click "Program To Device". Process takes approximately 5.3 seconds.

Disconnect USB-C cable.

Reconnect USB-C cable.

Plug in a working board with an ESPFlash header.

In terminal, run command:

    esptool.py -p /dev/tty.SLAB_USBtoUART flash_id

Observe:

 * Both TX and RX LEDs illuminate.
 * Target board resets.
 * Terminal reports the device ID, memory, etc of the working board.
