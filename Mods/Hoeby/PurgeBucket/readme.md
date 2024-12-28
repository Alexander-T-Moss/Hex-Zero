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
```
[gcode_macro CLEAN_NOZZLE]
variable_start_x: 128
variable_start_y: 55
variable_start_z: 3.6
variable_wipe_dist: 45
variable_wipe_count: 5
variable_wipe_speed: 10000
variable_raise_distance: 20

gcode:
 ## Check if extruder has minimum extrude temperature, otherwise heat extruder
 {% set temp_to_low = False %}
 {% set temp_min = printer.configfile.settings["extruder"].min_extrude_temp|float %}  

 ## Check if the target that is set on the extruder is larger then minimum extruder temp
 ## Otherwise heatup to minimum extruder temp
 {% if printer.extruder.target < temp_min %}
    M104 S{temp_min}
    {% set temp_to_low = True %} 
 {% endif %}
 
 ## Check if homing is done, otherwise homing
 {% if "xyz" not in printer.toolhead.homed_axes %}
   G28
 {% endif %}

 ## Check if Z_Tilt is done, otherwise Z_Tilt_Adjust
 {% if printer.z_tilt.applied == False %}
   Z_TILT_ADJUST
 {% endif %}

 ## There was no extruder target, waiting for extruder to finish heating to minimum extruder temp
 {% if temp_to_low == True %}
   M109 S{temp_min} 
 {% endif %}

 G90                                            

 ## Move nozzle to start position
 G1 X{start_x} Y{start_y} F{wipe_speed / 2}
 G1 Z{start_z} F1500

 ## Wipe nozzle
 {% for wipes in range(wipe_count) %}
    {% for coordinate in [(start_x, start_y),(start_x, start_y - wipe_dist)] %}
        G0 X{coordinate[0] - 0.6 * wipes} Y{coordinate[1]} F{wipe_speed}
    {% endfor %}
 {% endfor %}

 ## There was no extruder target, disable extruder heater
 {% if temp_to_low == True %}
   M104 S0 
 {% endif %}
  
 ## Raise nozzle
 G1 Z{raise_distance} F1500
 G1 X60 Y60 F{wipe_speed / 2}
