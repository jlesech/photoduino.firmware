           _                          _       _             
          | |           _            | |     (_)            
     ____ | |__   ___ _| |_  ___   __| |_   _ _ ____   ___  
    |  _ \|  _ \ / _ (_   _)/ _ \ / _  | | | | |  _ \ / _ \ 
    | |_| | | | | |_| || |_| |_| ( (_| | |_| | | | | | |_| |
    |  __/|_| |_|\___/  \__)\___/ \____|____/|_|_| |_|\___/ 
    |_|  THE OPENSOURCE CAMERA CONTROLLER BASED ON ARDUINO                                                         



#Photoduino firmware

This code is the firmware for Photoduino Shields (1.0, 2.0 and 3.0 hardware versions) as Arduino Sketch.

Visit the project site: <http://www.photoduino.com>

* * *

##Firmware changelog:

## release 0.11 (development version)

 - Compatible with the new software for desktop control [Photoduino Remote 0.1](https://github.com/Photoduino/photoduino.remote)
 - New language file with Italian translation of menus (Thanks to Andrea Candolini)
 
##release 0.10 (stable version)
[Download release 0.10](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.10.zip)

 - All files use ".ino" file extension for the 1.0 Arduino environment
 - Fixed some compile errors on Arduino 1.0 environment
 - Now uses progmem for allocating strings in program memory
 - Reduced compiled code size
 - New progress bar interface element
 - Added confirmation message when you reset config in any execution mode to avoid accidental losses
 - Fixed some spelling errors
 - Now the shutterlag is a common system parameter because it depends of the camera model and is the same in all the run modes. 
 - Now "Use flash1" and "Use flash2" are system parameters. If p.e. UseFlash2 is "NO", then in the config menus of all run modes you will don't see the "flash2 pretime".
 - Now, the language messages are in separated files for each language to improve future translations.
 - Mirror lockup timeout is now configurable through the system menu.
 - New system parameter "DEVICE TYPE" determines the use of the Device port like laser, electrovalve, ...
 - A big new functionality of control electro-valve or solenoid valve. Docs soon.
 - New key input holding A+B buttons to use it in numeric sensor tuning to match sensor and limit values to equal.
  
 
##release 0.9 
[Download release 0.9](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.9.zip)

 - Added new "Mirror lockup" functionality in all sensor modes
 - Added new "Numeric mode" for tuning sensor limit with more precision. 
 - Added compatibility with ArduinoMega by "#define BOARD_ARDUINO_MEGA".
 - Default interval time is now 1 second instead 1000 miliseconds because 
   is more common used.
 - Added a compile value to define the pulse width for shooting the flash.
 - Some other minor fixes and code reviews.  
 
##release 0.8
[Download release 0.8](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.8.zip)

 - Bug fixed on some cameras like canon 50d with prebulb yes. 
 
##release 0.7 
[Download release 0.7](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.7.zip)

 - Bug fixed on shutterEnd with prebulb yes. 
  
##release 0.6 
[Download release 0.6](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.6.zip)

 - New mode "Flash slave" uses the LDR sensor to shoot the flashes like a 
   slave flash.
 - Now all text messages are defines to make posible the i18n. 
   Current available languages are spanish and english
 - Fixed a bug with cycles on intervalmode
 
##release 0.5 
[Download release 0.5](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.5.zip)

 - Now each sensor have a run mode and custom config
 - New parameter "cycles" also on sensor trigger modes
 - New parameter "intercicle time" added on sensor trigger modes for wait
   between cycles to let the camera time to process the photo or avoid shoots
   by noise on sensors.
 - Removed all "exit" options from menus to reduce code size and simplify. 
   Use hold-A-button to exit.
 - Added power on/off control of a laser connected to the RESERVED port. 
   Laser is set power-off before open the camera shutter.
 - Re-organization of .pde files
 - Many code improvements to reduce code size and enhace the organization
 
##release 0.4
[Download release 0.4](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.4.zip)

 - Keyboard reading is completly re-writed code to enhance control and use 
   debounce and hold time
 - Revision of code comments
 - added reference of default shutterlag times for canon DSLR cameras
 - (function setSensorLimit) now uses two buttons for up and down the value
  
##release 0.3
[Download release 0.3](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.3.zip)

 - (function setIntValue) Bug fixed when sets numeric values higher than 59999 
 - (function setIntValue) Numeric values now uses two buttons for up and down 
 - (function setIntValue) Now shows the measure units
 - (PINS_BTN_A and PINS_BTN_B) Interchanged to be the same reference in silkscreen
 - (function keyScan) Bug fixed
 
##release 0.2
[Download release 0.2](https://github.com/downloads/Photoduino/photoduino.firmware/photoduino.shield.firmware.v.0.2.zip)

 - New file organization
 - Various improvements
 - Configuration backup on eeprom
 
