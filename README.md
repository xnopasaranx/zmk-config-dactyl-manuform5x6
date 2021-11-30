# zmk-config for Dactyl Manuform 5x6 (BLE, per key rgb, trackball on the right half.
dactyl manuform zmk firmware builder

This is my attempt at a dactyl manuform (5x6) zmk build. It has rgb underglow activated for 34 keys on the left side and 32 on the right (eventhough the right only has 28 leds), as I am using per key leds (SK6812 mini E). 
I am still in the testing stuff and configuring things phase, both halves are finished and tested as far as keymatrix and lighting are concerned.

I used the brilliant r-track dactyl manuform variant, designed by u/qqurn who has been so kind to share their design here: https://gitlab.com/keyboards1

Because I am using huge bricks for batteries I had to design a wristrest which also houses the powerpacks. The design was quickly thrown together in tinkercad and is probably neither perfect nor finished.

# To Do
* port my keymap from qmk
* map all leds to a somewhat more convenient array table, so I can address them
* configure bluetooth, powersaving options (vcc enable and disable when rgb is toggled...)
* configure how usb hid behaves together with bluetooth (button to choose, when usb is connected... how is second half connected. etc)
  * I really would like the second half to communicate with the primary half over ble even if it is plugged in to charge...
* the holy grail: somehow getting my shiny new pmw3360 sensor to work as a trackball...

# Bill of materials
* 62x MxLEDBitPCB single switch pcbs
 * see here https://github.com/swanmatch/MxLEDBitPCB 
 * (four switches of the right half will be mounted with only kailh hotswaps, as the pcbs will not fit together with the trackball)
* 62x SK6812 Mini-E rgb leds
 * right thumbcluster is unlit, no need for leds there
* 66x kailh hotswap sockets
 * 66x diodes (4 diodes will need to be soldered directly to the hotswap sockets on the right thumb cluster)
* one pmw3360 sensor breakoutboard for the trackball
* Trackball (I chose a replacement ball for the Logitech Trackman Optical Trackball, will need to verify that this one fits) 
* 2x nice!nano microcontrollers (or promicro-c/elite-c if you don't want bluetooth)
* 2x tiny buttons for the reset switches
* 2x toggle switches to break power from the batteries to the MCUs
* 2x Li-ion 3.7v battery packs (I use 6600mAh bricks... because if you want wireless and per key rgb, you need juice!)
* a whole lot of wire and dupont terminals for hooking everything up
* HOT GLUE!!!! ok be careful when using pva hot glue... You will have to mount the single switch pcbs on the inside somehow. Obviously wire everything up and test first! The hotswap sockets will be pushed down when inserting a new switch, if the pcbs have not been mounted with some bonding agent from the inside. There is probably a cleaner solution, but this is my keyboard so go somewhere else to complain ^^ 
