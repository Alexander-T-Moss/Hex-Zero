# &#x2B22; Waveshare 2.8 Screen Mount &#x2B22;
![image](https://github.com/Alexander-T-Moss/Hex-Zero/assets/54496326/f524ae10-6290-42b0-9079-dfc5f761cd1c)

Front skirt mount and cover for installing a [Waveshare 2.8 Screen](https://www.waveshare.com/2.8inch-dsi-lcd.htm)

<br>

## Required Hardware
| Name | Quantity |
| --- | --- |
| [Waveshare 2.8 Inch Display](https://www.waveshare.com/2.8inch-dsi-lcd.htm) | 1x |
| M2.5x6 BHCS | 4x |

<br>

## Waveshare 2.8 Software Configuration Guide
**These steps need to be followed prior to installing and setting up KlipperScreen like you would regularly**
1. Log into your Pi SSH terminal (e.g. using putty or similar) and type in `sudo nano /boot/firmware/config.txt`

2. At the bottom of the opened file, find the `[all]` section and add the following line: `sudo nano /boot/firmware/config.txt` (_see image below for what it should look like_)

![image](https://github.com/Alexander-T-Moss/Hex-Zero/assets/54496326/18b5b8c4-b712-4df9-898d-61078d501016)

Then press `CTRL + X` then `Y` and finally hit `ENTER` to save this addition to the file

3. Next, back in the command line, enter `sudo nano /boot/firmware/cmdline.txt`

4. At the beginning of that .txt file, insert at the start of the line `video=DSI-1:480x640e,rotate=90` (_see image below for what it should look like_)

![image](https://github.com/Alexander-T-Moss/Hex-Zero/assets/54496326/54407e4c-f834-404b-9ec0-22c531be7a96)

(_Make sure it's all one line!_)

Then save this change by pressing `CTRL + X` then `Y` and finally hitting `ENTER`

5. Now we need to create a monitor config by typing `sudo nano /usr/share/X11/xorg.conf.d/90-monitor.conf` into the command line

6. In this new file, paste in the following (if it's opened up a blank file:
```js
Section "Monitor"
    Identifier "DSI-1"
    # This identifier would be the same as the name of the connector printed by$
    # it can be "HDMI-0" "DisplayPort-0", "DSI-0", "DVI-0", "DPI-0" etc

    Option "Rotate" "left"
    # Valid rotation options are normal,inverted,left,right


    Option "PreferredMode" "640x480"
    # May be necessary if you are not getting your preferred resolution.
EndSection
```

7. Check the content of this file matches the below image

![image](https://github.com/Alexander-T-Moss/Hex-Zero/assets/54496326/aaff3a68-8c42-41d7-80d2-1ff40baebf74)

Then save this change by pressing `CTRL + X` then `Y` and finally hitting `ENTER`

8. Finally, we need to edit the libinput config, so enter into the command line `sudo nano /usr/share/X11/xorg.conf.d/40-libinput.conf`

9. In the file that opened, find the following section

![image](https://github.com/Alexander-T-Moss/Hex-Zero/assets/54496326/76f3bb85-11ed-4621-a481-893f1e0efa84)

And add the line `Option "TransformationMatrix" "0 -1 1 1 0 0 0 0 1"` above the `EndSection` indented to match the lines above, it should look like the image below

![image](https://github.com/Alexander-T-Moss/Hex-Zero/assets/54496326/e46864f8-7b00-470a-b67e-947fdcc04438)

10. Then save this change by pressing `CTRL + X` then `Y` and finally hitting `ENTER`

11. Reboot the pi by running `sudo reboot` in the command line then you can go about installing KlipperScreen like you would for any other display

Happy Printing!

<br>

## Credits
This display mount was initially created by [HartK](https://github.com/hartk1213/VoronUsers/tree/master/printer_mods/hartk1213/Voron0.2_2.8_WaveshareDisplay), then adapted by MechaXx for HX0, and finally tweaked by myself to integrate into the official HX0 CAD assembly. Thank you to MechaXx for initially implementing this into your HX0 build and writing the setup guide for the Waveshare 2.8!
