CAUTION! While this model file has been tested to the best of my ability and I have flown with it, use these files and information at your own risk! This model file will only operate properly if your receiver is configured the same as the system this model was created with. It will only work properly with an AR631/AR637 receiver that has been unlocked and reset allowing unlimited reprogramming of the safe modes, servo directions, model wing/tail type, etc. By using this model .yml file you accept all risk.  Failure to fully test all functions and pre-flight your model may result in a crash and possibly significant damage. Shane's DIY assumes no responsibility for damages to your equipment through the use of this information.

Model notes/requirements:
*Designed for unlocked Spektrum AR631/AR637 receivers.

*Wing type should be set for "Flaperon" and "Tail Normal" Rudder + Elevator. Left aileron is on receiver channel 2 (radio channel 1). Right aileron is on channel 5 on both receiver and radio.

*Model Setup: Protocol DSM X2F.  Multi module firmware v1.3.3.33 AETR, Channel Range 1-12, EdgeTX version was 2.9.4

*SE switch controls flap mix:
SG↑ = Flaps up.
SG- = Takeoff flaps (changes aileron rates to 150%)
SG↓ = Landing flaps (changes aileron rates to 200%)
NOTE: The 150 & 200% rates allow full aileron throws while flaps are deployed. Without this mix, aileron control is very minimal with flaps deployed which could result in insufficient control. Without this I do not like using flaperons.  The servos are not moving greater than 100% throw, you are only restoring full throws after the flaperon offset is active.

*SE switch on Channel 7 controls receiver F-Modes:
SE↑ =SAFE (auto level) / F-Mode 1
SE- =Mid rate (AS3X intermediate with bank limit) / F-Mode 2
SE↓ =High rate (AS3X) / F-Mode 3
NOTE: The 3 "safe" modes can be customized through forward programming. Channel 7 must be set in your receiver as the F-Modes channel. No PANIC mode is used on this model

*SF↑ is throttle active (must reduce throttle stick to -100 to enable)
SF↓ is throttle cut

*SH switch on channel 8 controls reverse thrust:
SH↓ and hold is "auto reverse thrust". If throttle is active and the throttle stick is at -100 (minimum) reverse will automatically activate and go to the preset throttle level. Radio calls out "brakes on" while holding. Special Function SF14 is set to +100 to equal full reverse thrust while holding SH↓ for more than 1 second. Editing SF14 to lower than +100 will reduce the max reverse thrust.  For manually controlled reverse thrust for ground control, water operations, etc. switch SB- or SB↓ activates reverse thrust and the throttle stick will control the throttle level from 0-100%. SB↑ enabled forward thrust.  Custom curve "CV1:RCV" is "Reverse curve" which is used to set the output of the three positions of the SB switch and prevent a channel 8 from outputting a value of '0'.
NOTE: Reverse thrust requires that you have an Avian ESC with reverse programmed to channel 8. If you do not have the Avian ESC or it has not been set up, holding SH will trigger full forward throttle if the throttle is not cut!  SB will have no effect and only forward thrust is available.

*If you have an Avian ESC, flight pack voltage telemetry will be available. Logical switch L03 monitors telemetry value "EVIN" and turns on L03 if the voltage drops below 11.40v for greater than 15 seconds. This triggers Special Function SF18 to Play the "lobatt.wav" track every 20 seconds.

*Trim Switch 6U (pressing T6↑) will reset the flight telemetry, timer 1, and timer 2.

*In telemetry tab, "Disable telemetry alarms" has been activated to eliminate nuisance alarms due to Spektrums short range telemetry.

*The display "Top Bar" widgets used to dislay "Flaps" position and "Rates" in text format is called "SwitchPRO" and it is included in this zip file. Copy the SwitchPRO folder into your SD Card /WIDGETS/ folder if you do not already have it.

*A nice AeroScout image file has been included.  Copy the "AeroScout.png" image file into your SD card /IMAGES/ folder if desired.

========================================

INSTALLATION/SETUP INSTRUCTIONS:
1) Extract the .zip file to a location of your choice.

2) If desired, copy the /SOUNDS/en folder into your SD card. You can copy the individual .wav files directly to your SD Card "/SOUNDS/en" folder or drop the supplied folder into your SOUNDS folder and it will add the supplied .wav files if done properly. If files of the same name exist in your SD card you will be asked if you wish to overwrite. You can change the audio call outs, I've included mine in case you wish to use them.

3) View your existing SD Card /MODELS/ folder and select an unused "models##.yml" file name.  Rename the "AeroScoutFlap.yml" file to "model##.yml" (replace the ## with an unused model number) and copy it into your /MODELS/ folder.  When you cycle power on your radio, it will automatically add it to your "labels.yml" models index file and it should be available to open. If it does not appear, you may have to change the "labels" your models folder is displaying if it is not assigned a label yet.

4) For detailed model setup information extracted from Companion review the "AeroScoutFlap Config.pdf" file.

