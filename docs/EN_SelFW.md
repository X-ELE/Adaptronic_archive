  
  
  
  
  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  
  
  
  
  
  

Select Firmware Revision History

[go back to support
                home](EN_EUGENE_HOME.md)  

![image](../images/Eugene/Eugene250.png)
  
  

  

  

[Eugene
                current release changelog.  

              ](file:///C:/New%20Help/EN_EUGENE_RELEASE_NOTES.md)

[Eugene previous release changelog.](file:///C:/New%20Help/EN_EUGENE_PREVIOUS.md)

[Modular
                firmware changelog history](file:///C:/New%20Help/EN_ModFW.md)[](EN_SelFW.md)

[  

              ](EN_SelFW.md)

  

  
  
v15.021  
Released
                      2017-Jan-26  

- Changed
                        default streaming state
- Implemented
                        variable off-time for injectors for 3 stage
- Allowed
                        variable off-time for injectors
- Allowed
                        1UZFE VVT more than +45 degrees advance
- Fixed
                        dig in bug introduced in 15.016
- Added
                        option for aux logic to read digital inputs
- Checked
                        Seq6 ignition mode during cranking for XR6v15.013  
Released 2017-Jan-26  

- Slowed
                        down SRT4 comms
- Fixed Innovate SSI4
                    votlage input
- Added special code to
                  avoid final entry in timing table being the new TDC point on
                  missing tooth triggers
- Changed serial streaming
                  code
- Added special case for 100
                  % ignition cut. Made serial output stream by default on serial
                  out port
- Stopped allowing negative
                  PID gains for VVT
- Increased AC input
                  debouncs from 20 loop cycles to 100 (approx 1/3 sec)
- Added 2/3/4 cylinder tacho
                  output (select invert on 4/6/8 cylinders)
- Added code to lock out
                  adaptive fuel and flex fuel from e420d
- Moved Suzuki cam-only
                  trigger back to its own setting (Requires new WARI)
- Added Suzuki cam-only
                  trigger - set it to Honda Jazz though
- Changed 3D bosot behaviour
                  so in gear/ digital input mode it doesn't clip by boost Dc /
                  gear separately
- Added
                        support for Innovate PSB (only looks at lambda)  

  
  
©2018
        Adaptronic  
  
