# Edgewater High School FolgerTech 2020 Prusa i3

<a href="https://edgewaterhs.ocps.net/academics_and_curriculum/e_s_t_magnet/vision__mission__goals">
<img align="right" src="./img/est-250.png" alt="Engineering, Science, and Technology"/>
</a>

This repository contains the firmware and documentation for Edgewater's student-made 3D printer. It was created with the understanding that future students may wish to repair, updgrade, update, or simply learn about the printer. It is also meant to serve as a resource for instructors, who can use it to teach about the printer, GitHub, or 3D printing in general. That said, this resource is not meant to be exhaustive; 3D printers require research and troubleshooting skills when new problems arise and that simply can't be reflected here. Listed below are some important notes to keep in mind as well as some helpful links.  

## Before print (tmp name)  
what to do before a print job (kapton, glue, leveling, etc.)

## After print (tmp name)  
what to do after a print job (removing, evaluating, cleaning up prints, etc)

## Upgrades and maintenance  
The printer can be considered finished, but as with any DIY project, there is still much room for improvement. RepRap printers in particular have whole communities dedicated to upgrading them. Simply by searching "FolgerTech 2020 upgrades," you can find numerous collections and forum posts dedicated to what others have done. Care must be taken however, in applying these upgrades yourself; the printer can easily be rendered inoperable if thoughtlessly disassembled. With every miniscule change in hardware can come a drastic change in print quality. It is therefore necessary to understand what goes into setting up and maintaining a 3D printer before you can upgrade one.

Regular maintenance is also required by any 3D printer. As such, the [build](./doc/FolgerTech-2020-i3-Build-Manual-Rev-A.pdf) and [software](./doc/FolgerTech-2020-i3-Config-Guide-1-1.pdf) setup guides are included should anything need to be revisited. Keep in mind that these documents are dated and should be taken with a grain of salt. The hardware and electronics configuration may be the same but the software might have changed. Aside from tightening screws once in a while, the print bed may need to be leveled from time to time. In addition, the build plate may need to be cleaned of any accumulated dust or grease.

## Common troubleshooting issues  
The nut that holds the right part of the x-carriage up on the threaded rod may sometimes fall out and cause the x-carriage to become tilted. Turn off the z-axis stepper motors (IMPORTANT!!! if this is not done there will be a spark and possibly electrical damage when completing the next steps). Hold the stepper motor still and turn the right nut until it is touching the x-carriage. Lift the x-carriage slightly and continue to turn the nut until it can be reseated in the plastic piece. Continue by turning the stepper motor until the x-carriage is level. The bed may have to be releveled after this. Since the x-carriage may not be level, it can be helpful to play around with the height of each end of the x-carriage (again, turn the stepper motors off and then move them manually to lower/raise either end).

The connectors for the thermistors (pairs of white wires) are faulty and may not give a reading for either the temperature of the bed or the extruder. They can simply be removed, the wires reseated, and then replaced. Advice for permanent fix: crimp new connectors, in particular for the rightmost thermistor.

## Updating the firmware  
not complete

Marlin site: http://marlinfw.org/


FolgerTech files: [Google Drive](https://drive.google.com/drive/folders/0B9b1NbuMK524fldIWWVCa0xfSXAtZmttcDhrbjBMeFNWcENBdVUzWnhtWDZ2YWdHVXpoUXM)  
FolgerTech store: [FolgerTech.com](https://folgertech.com/products/folger-tech-reprap-2020-prusa-i3-full-aluminum-3d-printer-kit)  

## Auto-bed-leveling 
Talk about the hardware in place, how it can be used, how not to use it

## !! Arduino Mega Issue !!  

The arduino mega's voltage regulator may be broken. In effect, the 3D printer is not able to run without a USB cable connected to it. This may or may not be a problem depending on the setup in use, but it would, at the very least, defeat the purpose of having an LCD controller with SD card support. 

There are a few different options (listed from least to most complex):  
- Do nothing. Leave the printer connected to the computer when it's in use until it can be fixed.
- Buy a new or use a different arduino mega (or compatible board) and replace the printer's. Put the old arduino aside to be used or repaired at another time.
- Hack a solution with a USB cable and LM7805. Connect an LM7805 to the power supply and a cut open USB cable to provide 5V to the printer. 
- Replace the regulator with the appropriate AMS1117. Order the surface-mount component and solder it on the board.  
- Attempt to replace the regulator with a readily available LM7805. Look at the circuit's topology and determine if it is compatible. Solder the pins to the small surface-mount pads in the appropriate order.


## To-do:  
- Calibrate 3D printer  
- Obtain consistent prints  
- Make a to-do for future/possible upgrades including links  
- Make a list of useful resources for future technicians  
- Update README and order appropriately  
- Add an LCD holder  
- Add a switch for the power supply  
- Add a tensioner for the x-axis  
- Add anti-backlash support for the z-axis  
- Add cooler for hotend (may have to move auto-bed-level part for this)  
- Add z-axis motor standoffs  
- Redo wiring, potentially with cable chains  
- Think of/find more upgrades