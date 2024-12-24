# PrugeBucket for HexZero, mantaray and hammerhead bed compatible
<p align="center"><img width="500" src="assets/PurgeBucket.png"></p>

## Which 3d parts are shared
Only the 3D printed parts for the PurgeBucket are shared. <br>
The bed-mount is mantaray and hammerhead bed compatible.

## Hardware needed for this mode
- 2x M3x8
- 2x M3 nut
- 2x Magnet 6x3
- 1x Nozzle silicone brush (Bambu A1)

## Printing advice
The advice is to print the bucket with support. <br>
There isn't a drawn support in the file. <br>
Without a support, the magnet hole for the bucket could be deformed.

## Used klipper macro
This macro is used to clean the nozzle. <br>
It assums, that the nozzle is already heated, there isn't a check on that. <br>
```[gcode_macro CLEAN_NOZZLE]
variable_start_x: 128
variable_start_y: 55
variable_start_z: 3.6
variable_wipe_dist: 45
variable_wipe_count: 5
variable_wipe_spd: 10000
variable_raise_distance: 20

gcode:
 ## Check if homing is done, incl. Z_til_adjust
 {% if "xyz" not in printer.toolhead.homed_axes %}
   G28
 {% endif %}
 {% if printer.z_tilt.applied == False %}
   Z_TILT_ADJUST
 {% endif %}
 G90                                            

 ## Move nozzle to start position
 G1 X{start_x} Y{start_y} F{wipe_spd / 2}
 G1 Z{start_z} F1500

 ## Wipe nozzle
 {% for wipes in range(wipe_count) %}
    {% for coordinate in [(start_x, start_y),(start_x, start_y - wipe_dist)] %}
        G0 X{coordinate[0] - 0.5 * wipes} Y{coordinate[1]} F{wipe_spd}
    {% endfor %}
 {% endfor %}

 ## Raise nozzle
 G1 Z{raise_distance} F1500
