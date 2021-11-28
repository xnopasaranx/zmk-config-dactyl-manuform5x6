# zmk-config
dactyl manuform zmk firmware builder

This is my attempt at a dactyl manuform (5x6) zmk build. It has rgb underglow activated for 34 keys on each side, as I am using per key leds (SK6812 mini E). 
I am still in the testing stuff and configuring things phase and only the left half of the keyboard is finished. Now that I have a proof of concept, I will finish handwiring
the right half and then continue to port over my keymap from my other dactyl manuform which runs qmk.

# To Do
* port my keymap from qmk
* map all leds to a somewhat more convenient array table, so I can address them
* configure bluetooth, powersaving options (vcc enable and disable when rgb is toggled...)
* configure how usb hid behaves together with bluetooth (button to choose, when usb is connected... how is second half connected. etc)
  * I really would like the second half to communicate with the primary half over ble even if it is plugged in to charge...
* the holy grail: somehow getting my shiny new pmw3360 sensor to work as a trackball...
