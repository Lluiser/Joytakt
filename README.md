# Joytakt
gamepad control over Elektron Syntakt via Max/MSP

![screenshot](https://github.com/Lluiser/Joytakt/blob/main/screenshot.jpeg?raw=true)


setup:  
tested on Mac but should work on Windows too  
requires a Syntakt connected via USB or midi in and out, an xbox series X controller and max/msp.   
ensure ST tracks are set to midi channels 1-13  
ensure ST can send and receive midi CCs over the right port  
turn on ST and gamepad. open Joytakt.maxpat  
click the 'midi setup' button, then double click the midiin and midiout objects and ensure they are set to the ST midi channels.  

/////////

usage:  
the patch consists of two sides, one for controlling ST macros (pitchbend, modwheel, breath and aftertouch) and another for controlling various mutes.

macros:  
these need to be configured on the ST on a track by track basis. sound > setup, then turn pitch bend depth to 0 (to avoid the pbn macro changing your pitch).  
scroll down and edit the desired macro. these can be copied and pasted to speed up cloning assignments to different tracks.  
The macros are mapped as follows: left stick (pitch bend bipolar, up and down) right stick (breath) modwheel (left trigger) and aftertouch (right trigger)  
press [X] to latch all macros at their current location. press [A] to unlatch. they won't bounce back until you move each joystick/trigger so this can be used to freeze macros independently while the others are still modified.

mutes:  
[LB] and [RB] each mute 4 different tracks while held - FX track is excluded  
hold then press [Y] to latch, and press [Y] again to unlatch. Both groups can be latched independently.  
gamepad mutes will ignore any tracks that have been manually muted on the ST.  
press [☰] (start) to re-shuffle the mutes, giving you 4 new channels per button.  
press [B] to unmute all muted tracks, including the FX track and any tracks that were manually muted on the ST.  
