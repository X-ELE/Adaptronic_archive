  
  
  
  
  
  
  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  
  
  
  
  
  

Turbo Speed Sensors on Modular ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)  

![image](../images/Eugene/Eugene250.png)
  
  
  

[Twin
                Turbo Control](EN_MOD_016_TWINTURBO.md)[ ](EN_EUGENE_ABOUT.md)

[How
                to Setup Open Loop Boost Control  

              ](EN_MOD_039_OPENLOOPBOOSTCONTROL.md)

  

[  

              ](EN_SelFW.md)

  

  
  
  
  
  
  
  
  
  
Increasingly recently, people have
                  started to install turbo speed sensors to monitor the rotor
                  speed of their turbochargers. I’m not sure if the goal here is
                  more data to monitor spool, configure antilag or just to make
                  sure that you’re not overspeeding the turbo, but many people
                  have asked for the ability to measure turbo speed and record
                  it on the ECU, so we’ve added it for some specific types of
                  sensors.  
  
The ECU supports up to 2 turbo speed sensors so that
                  you can measure the turbo speed of two separate turbochargers.
                  If in the future we build the turbo speed into either exhaust
                  back pressure monitoring or part of the boost control
                  algorithm, then turbo 1 will correspond to the odd bank, or
                  the front half of the engine in a twin-turbo inline 6 eg the
                  RB26DETT, and turbo 2 will correspond to the even bank or the
                  rear half of an inline.  
  
The inputs that can be used have to be high speed
                  frequency inputs; so normal digital inputs or[analogue
                    inputs](EN_MOD_008_INPUTS.md)are not suitable.  
  
These are:
- CAS2, if you’re not using it already for part
                      of the engine triggering
- CAS3, if that’s not being used for the engine
                      trigger or flex fuel
- CAS 4 or 5, if a Mini RT input module is
                      installed
- Flex / frequency input on the Mini RT module
- Any of the 3 VSS inputs on the Mini RT module
- The main VSS input, if it’s not being used for
                      vehicle speed.  
The selection of the source for the input is made on
                  the Turbo speed sensor setup page.  
  
The type of sensor should also be selected.
                  Currently we support the following options:
- Borg Warner EFR, 67mm compressor (with 12
                      blades). In this case, the sensor outputs 1 pulse for
                      every 8 blades, which means that the sensor gives out 1.5
                      pulses per revolution
- Borg Warner EFR, larger than 67mm compressor
                      (with 14 blades). Again in this case the sensor outputs 1
                      pulse for every 8 blades, which means 1.75 pulse per
                      revolution
- Honywell / Garrett with a bar type trigger, ie
                      2 pulses pre revolution  
The above sensors all give a digital output, so the
                  ECU must have that input selected as a digital input.  
  
Once the turbo speed input has been selected, it
                  will appear in the main gauge window and of course you can add
                  it to your own gauge page or to the monitor panel on the right
                  hand side, use it as a variable in your built-in scope to
                  watch spool rates and so on.  
  
Thank you.  
  
  
©2018
        Adaptronic  
  
