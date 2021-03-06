**CONTACT ANYCUBIC SUPPORT FIRST!** This should be your first point of contact for faulty machines, some of the fixes here may void you warranty, proceed at your own risk!

These issues / solutions have been compiled from cases reported by photonsters in photon owners group on facebook.

---

## KNOWN ISSUES

- USB names must be kept short and avoid special chars since photon cannot read them. found by [Michael Lippert](https://www.facebook.com/groups/AnycubicPhoton/permalink/1370647173079921/)
- Faulty internal USB cable ( bad connection, causing random resets )
- Random reset possibily caused by internal memory buffer issue
- z-wobble
- bad usb stick (stock stick)
- bad psu brick (models before yellow windows)
- machine reset / reboot
- machine freezes mid print (usually usb related)
- half screen
- flickering screen during print 
- screen cable sheering on transport
- mainboard failure ( how to test video ) https://youtu.be/F69UMKYKvbY
- memory errors
- dead z axis
- failure to set homing offset values ( config.gcode issue reflash config.gcode )
- layers shifting on LCD during print ( possible cause is defective chip on mainboard )
- loose print bed head / print head too short ( plate assembly issue )
- slicer does not display STL ( PC Gfx board driver issue )
- z motors stops moving mid print, LCD keeps exposing resin, no error message, stopping print and moving z via menu works.

---
### Random resets / Memory errors / USB Read problems
#### Symptoms
- Printing freezes at random points, resets to homescreen
- Random freezes with error code
- File browser not displaying any models
- USB key light indicator is off, but plugged in ( it should always be on )
- If you wiggle the USB Key, you can read files again

#### How to fix
- replace stock USB key with >16gb one, format to Fat32
- Only have one file on USB, using short name and no non english characters or spaces.
- If problem still occurring you might have defective USB extension cable or faulty mainboard.
- video instructions for checking USB cable - https://www.youtube.com/watch?v=6JowsfJEdHs
- Test with a new USB Extension cable. this is male to female type, you can easily access this by removing the four screws holding the rear vent. UNPLUG POWER BEFORE DOING THIS
 Unplug the male connector to the mainboard and plug in a replacement, then plug in your USB key. If this fixes the problem, contact Anycubic for a replacement cable as it uses a special external mount.
- If you have a small USB key, you can plug it directly to the mainboard for testing, I would not recommend it as permanent solution. 
- If the problem does not solve with replacement USB cable, then you might have a faulty mainboard. Contact Anycubic immediately for a replacement or new machine. Firmware updates will not solve the USB issue.
- Update 15-07-18 : before printing try to remove power cable with no USB plugged in, wait for 1 min then plug power and USB back in. Possible cause might be IC Memory buffer issue, unplug the power should reset it.
- Check printer driver reference voltage is between 1.07 and 1.16v if not tune it to that how to in [here](https://www.facebook.com/groups/AnycubicPhoton/permalink/1404990436312261/) confirmed by Laszlo Cook

### Slicer wont display model / doesnt work
Photon Slicer currently does not support intergrated graphic driver, or resolution above 2k.

### Loose print bed head / print head too short
#### Symptoms
- The printhead tilts side to side even when mount screw is tightened,
- The print head sits too high from the FEP and can not lower any more.
Photo of the print bed assembly here - https://github.com/Photonsters/anycubic-photon-docs/blob/master/known-issues/photon_bed_mount_assembly.jpg

#### How to fix
- Dissamble build plate assembly and resit ball joint - https://www.youtube.com/watch?v=VdiNI_Xu6bI
- Check your build plate mount screws Tutorial > https://www.youtube.com/watch?v=Uc8senzACFM
- remove the mount screw
- remove the four screwes holding the print bed
- three more screws inside that will help tighten the ball joint have a look in there.
- CLEAR OUT ANY RESIN WITH IPA.
- they should be tight. Some users report that grinding, cutting the screws all it to sit tighter, be careful.
- re align and adjust the length of the printhead. 
- If you can't tighten down the build plate with the grub screw, Remove the four screws holding the ball joint in place and have a look inside there are 3 more screws and it may be that they are loose tighten them up again and off you go.

### Z Wobble / non random layer artifacts 
#### Symptoms
- non random layer artifacts visible on print no matter oreintation of print
- Consistent warped prints

#### Causes and fixes
 - Loose FEP - Tighten Fep https://youtu.be/Sdxf9mf7-ns
 - Replace FEP https://youtu.be/DLi3chV43LQ
 - Z Axis video fix (adjusting the wheels on the carriage)https://www.youtube.com/watch?v=4cfCWmHtsy8
 - Loosened the Z Axis stepper motor mounting screws twice (different degrees each time)
 - Taken the brass seating fixture out of the carriage and reseated it for a smooth fit
 - Taken the Z Axis screw out completely and reinstalled it
 - Grease Z rod
 
 ### layers shifting on LCD during print 
 #### Symptoms
 - prints look like they have been sliced / cut and moved onto another part of the build plate
 - Checking the photon file reveals no problems ( use photonFileValidator ) 
 
 #### Causes and fixes
 - LCD or mainboard defact - perform 'dry run' and use timelapse camera to check if the LCD shifts during print.
 - UNCONFIRMED FIX - Suggest contact Anycubic with evidence of issue first. check all cables are tight, Update Firmware.
 - Check cables are secure and not loose during shipping.
 
  ### Photon slicer does not display STL
  - Update display driver.
  
  ### Photon slicer does not run
  - ReInstall C++ distribution library
  - ReInstall slicer
  https://support.microsoft.com/en-au/help/2977003/the-latest-supported-visual-c-downloads
 
 ### LCD displpays only half of the model
 #### Symptoms
 - LCD displays half model, viewing display shows correctly.
 - this is not related to flickering LCD
 
  #### Causes and fixes
  - check cables
  - contact anycubic
  - update firmware from anycubic support site 
 
 ### Other random problems with a combination of the above
 #### Symptoms
 - After you have tried all the fixes above, machine is still behaving abnormally, this could be a faulty Mainboard.
 
  #### Causes and fixes
 - Check for mainboard faults using mulitmeter following this video https://youtu.be/F69UMKYKvbY
 - Replace Mainboard.
 
## Error codes
#### M_11820
Machine will randomly freeze during print and display error, Z does not retract, fan stays on.

#### M_11800
From Anycubic engineer 'this means USB is not plugged in'

#### M_11000
USB Read problem, Buy new USB, 8GB or less FAT 32. ( sandisk reported fixed issue )
