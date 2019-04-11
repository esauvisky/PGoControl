PGoControl
==========

**Script that automates and facilitates spoofing in Pokémon Go, remotely controlling Android devices via a PC.**

_Backup and switch features require a rooted device. Pointer Location might as well._

## Features and Usage:

    -d,  --device [ID]      Selects which device to use (see adb devices).
                                  If not passed, all devices are used simultaneously.
                                  If it's a integer number, uses only the nth device listed.
                                  
    -f,  --fetch-clipboard Syncs clipboard from device -> to computer.
                                  Requires Android 7 or higher and clipper installed.
                                  
    -p,  --paste-clipboard Syncs the clipboard from computer -> to device, while pasting.
                                  Requires Android 7 or higher and clipper installed.
                                  
    -l, --pointer-location Toggles pointer-location (tracking) on the device(s).
         
    -t, --auto-teleport    Teleports all connected devices to any coordinate in your clipboard.
         
    -s, --switch           Makes a backup of the current profile, and switches to a new one.
                                  Useful for using multiple accounts, as all your data (incl. teams,
                                  sound configs, etc) will actually be backed up as well.
                                  
    -b, --backup           Makes a backup of the current profile.

### Examples:

1. Auto teleport all devices connected to `adb`

   **This assumes you're using [GPS Joystick](http://gpsjoystick.theappninjas.com) by TheAppNinjas.**
   - Add a key shortcut configured to run `PGoControl -t`
   - Copy any coordinate on your computer.
   - Press the key combination: all connected devices will teleport to the coordinate in your clipboard.
   *You can also add more than one shortcut, one for each device (eg.: Ctrl+Shift+1, Ctrl+Shift+2) and pass the -d argument for each one, with `PGoControl -t -d 1`*

2. Send you PC clipboard and paste it into the device:

   **This assumes you have [clipper](https://github.com/majido/clipper) installed into your device.**
   - Add a key shortcut to `PGoControl -p`
   - Copy any text
   – Press the key combination: all connected devices will paste the text you had on your PC's clipboard.

_And so on..._
