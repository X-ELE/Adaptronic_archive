Modular Firmware Revision History/*

Copyright (c) 2008, Yahoo! Inc. All rights reserved.

Code licensed under the BSD License:

http://developer.yahoo.net/yui/license.txt

version: 2.6.0

*/

html{color:#000;background:#FFF;}body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,code,form,fieldset,legend,input,textarea,p,blockquote,th,td{margin:0;padding:0;}table{border-collapse:collapse;border-spacing:0;}fieldset,img{border:0;}address,caption,cite,code,dfn,em,strong,th,var{font-style:normal;font-weight:normal;}li{list-style:none;}caption,th{text-align:left;}h1,h2,h3,h4,h5,h6{font-size:100%;font-weight:normal;}q:before,q:after{content:'';}abbr,acronym{border:0;font-variant:normal;}sup{vertical-align:text-top;}sub{vertical-align:text-bottom;}input,textarea,select{font-family:inherit;font-size:inherit;font-weight:inherit;}input,textarea,select{*font-size:100%;}legend{color:#000;}del,ins{text-decoration:none;}body{font:13px/1.231 arial,helvetica,clean,sans-serif;*font-size:small;*font:x-small;}select,input,button,textarea{font:99% arial,helvetica,clean,sans-serif;}table{font-size:inherit;font:100%;}pre,code,kbd,samp,tt{font-family:monospace;*font-size:108%;line-height:100%;}body{text-align:center;}#ft{clear:both;}#doc,#doc2,#doc3,#doc4,.yui-t1,.yui-t2,.yui-t3,.yui-t4,.yui-t5,.yui-t6,.yui-t7{margin:auto;text-align:left;width:57.69em;*width:56.25em;min-width:750px;}#doc2{width:73.076em;*width:71.25em;}#doc3{margin:auto 10px;width:auto;}#doc4{width:74.923em;*width:73.05em;}.yui-b{position:relative;}.yui-b{_position:static;}#yui-main .yui-b{position:static;}#yui-main,.yui-g .yui-u .yui-g{width:100%;}{width:100%;}.yui-t1 #yui-main,.yui-t2 #yui-main,.yui-t3 #yui-main{float:right;margin-left:-25em;}.yui-t4 #yui-main,.yui-t5 #yui-main,.yui-t6 #yui-main{float:left;margin-right:-25em;}.yui-t1 .yui-b{float:left;width:12.30769em;*width:12.00em;}.yui-t1 #yui-main .yui-b{margin-left:13.30769em;*margin-left:13.05em;}.yui-t2 .yui-b{float:left;width:13.8461em;*width:13.50em;}.yui-t2 #yui-main .yui-b{margin-left:14.8461em;*margin-left:14.55em;}.yui-t3 .yui-b{float:left;width:23.0769em;*width:22.50em;}.yui-t3 #yui-main .yui-b{margin-left:24.0769em;*margin-left:23.62em;}.yui-t4 .yui-b{float:right;width:13.8456em;*width:13.50em;}.yui-t4 #yui-main .yui-b{margin-right:14.8456em;*margin-right:14.55em;}.yui-t5 .yui-b{float:right;width:18.4615em;*width:18.00em;}.yui-t5 #yui-main .yui-b{margin-right:19.4615em;*margin-right:19.125em;}.yui-t6 .yui-b{float:right;width:23.0769em;*width:22.50em;}.yui-t6 #yui-main .yui-b{margin-right:24.0769em;*margin-right:23.62em;}.yui-t7 #yui-main .yui-b{display:block;margin:0 0 1em 0;}#yui-main .yui-b{float:none;width:auto;}.yui-gb .yui-u,.yui-g .yui-gb .yui-u,.yui-gb .yui-g,.yui-gb .yui-gb,.yui-gb .yui-gc,.yui-gb .yui-gd,.yui-gb .yui-ge,.yui-gb .yui-gf,.yui-gc .yui-u,.yui-gc .yui-g,.yui-gd .yui-u{float:left;}.yui-g .yui-u,.yui-g .yui-g,.yui-g .yui-gb,.yui-g .yui-gc,.yui-g .yui-gd,.yui-g .yui-ge,.yui-g .yui-gf,.yui-gc .yui-u,.yui-gd .yui-g,.yui-g .yui-gc .yui-u,.yui-ge .yui-u,.yui-ge .yui-g,.yui-gf .yui-g,.yui-gf .yui-u{float:right;}.yui-g div.first,.yui-gb div.first,.yui-gc div.first,.yui-gd div.first,.yui-ge div.first,.yui-gf div.first,.yui-g .yui-gc div.first,.yui-g .yui-ge div.first,.yui-gc div.first div.first{float:left;}.yui-g .yui-u,.yui-g .yui-g,.yui-g .yui-gb,.yui-g .yui-gc,.yui-g .yui-gd,.yui-g .yui-ge,.yui-g .yui-gf{width:49.1%;}.yui-gb .yui-u,.yui-g .yui-gb .yui-u,.yui-gb .yui-g,.yui-gb .yui-gb,.yui-gb .yui-gc,.yui-gb .yui-gd,.yui-gb .yui-ge,.yui-gb .yui-gf,.yui-gc .yui-u,.yui-gc .yui-g,.yui-gd .yui-u{width:32%;margin-left:1.99%;}.yui-gb .yui-u{*margin-left:1.9%;*width:31.9%;}.yui-gc div.first,.yui-gd .yui-u{width:66%;}.yui-gd div.first{width:32%;}.yui-ge div.first,.yui-gf .yui-u{width:74.2%;}.yui-ge .yui-u,.yui-gf div.first{width:24%;}.yui-g .yui-gb div.first,.yui-gb div.first,.yui-gc div.first,.yui-gd div.first{margin-left:0;}.yui-g .yui-g .yui-u,.yui-gb .yui-g .yui-u,.yui-gc .yui-g .yui-u,.yui-gd .yui-g .yui-u,.yui-ge .yui-g .yui-u,.yui-gf .yui-g .yui-u{width:49%;*width:48.1%;*margin-left:0;}.yui-g .yui-g .yui-u{width:48.1%;}.yui-g .yui-gb div.first,.yui-gb .yui-gb div.first{*margin-right:0;*width:32%;_width:31.7%;}.yui-g .yui-gc div.first,.yui-gd .yui-g{width:66%;}.yui-gb .yui-g div.first{*margin-right:4%;_margin-right:1.3%;}.yui-gb .yui-gc div.first,.yui-gb .yui-gd div.first{*margin-right:0;}.yui-gb .yui-gb .yui-u,.yui-gb .yui-gc .yui-u{*margin-left:1.8%;_margin-left:4%;}.yui-g .yui-gb .yui-u{_margin-left:1.0%;}.yui-gb .yui-gd .yui-u{*width:66%;_width:61.2%;}.yui-gb .yui-gd div.first{*width:31%;_width:29.5%;}.yui-g .yui-gc .yui-u,.yui-gb .yui-gc .yui-u{width:32%;_float:right;margin-right:0;_margin-left:0;}.yui-gb .yui-gc div.first{width:66%;*float:left;*margin-left:0;}.yui-gb .yui-ge .yui-u,.yui-gb .yui-gf .yui-u{margin:0;}.yui-gb .yui-gb .yui-u{_margin-left:.7%;}.yui-gb .yui-g div.first,.yui-gb .yui-gb div.first{*margin-left:0;}.yui-gc .yui-g .yui-u,.yui-gd .yui-g .yui-u{*width:48.1%;*margin-left:0;} .yui-gb .yui-gd div.first{width:32%;}.yui-g .yui-gd div.first{_width:29.9%;}.yui-ge .yui-g{width:24%;}.yui-gf .yui-g{width:74.2%;}.yui-gb .yui-ge div.yui-u,.yui-gb .yui-gf div.yui-u{float:right;}.yui-gb .yui-ge div.first,.yui-gb .yui-gf div.first{float:left;}.yui-gb .yui-ge .yui-u,.yui-gb .yui-gf div.first{*width:24%;_width:20%;}.yui-gb .yui-ge div.first,.yui-gb .yui-gf .yui-u{*width:73.5%;_width:65.5%;}.yui-ge div.first .yui-gd .yui-u{width:65%;}.yui-ge div.first .yui-gd div.first{width:32%;}#bd:after,.yui-g:after,.yui-gb:after,.yui-gc:after,.yui-gd:after,.yui-ge:after,.yui-gf:after{content:".";display:block;height:0;clear:both;visibility:hidden;}#bd,.yui-g,.yui-gb,.yui-gc,.yui-gd,.yui-ge,.yui-gf{zoom:1;}h1 {
  font-size: 138.5%;
}

h2 {
  font-size: 123.1%;
}

h3 {
  font-size: 108%;
}

h1, h2, h3 {
  margin-top: 1em;
  margin-right: 0px;
  margin-bottom: 1em;
  margin-left: 0px;
}

h1, h2, h3, h4, h5, h6, strong {
  font-weight: bold;
}

abbr, acronym {
  border-bottom-width: 1px;
  border-bottom-style: dotted;
  border-bottom-color: black;
  cursor: help;
}

em {
  font-style: italic;
}

blockquote, ul, ol, dl {
  margin-top: 1em;
  margin-right: 1em;
  margin-bottom: 1em;
  margin-left: 1em;
}

ol, ul, dl {
  margin-left: 2em;
}

ol li {
  list-style-type: decimal;
  list-style-image: none;
  list-style-position: outside;
}

ul li {
  list-style-type: disc;
  list-style-image: none;
  list-style-position: outside;
}

dl dd {
  margin-left: 1em;
}

th, td {
  border-top-width: 1px;
  border-right-width: 1px;
  border-bottom-width: 1px;
  border-left-width: 1px;
  border-top-style: solid;
  border-right-style: solid;
  border-bottom-style: solid;
  border-left-style: solid;
  border-top-color: black;
  border-right-color: black;
  border-bottom-color: black;
  border-left-color: black;
  -moz-border-top-colors: none;
  border-top-colors: none;
  -moz-border-right-colors: none;
  border-right-colors: none;
  -moz-border-bottom-colors: none;
  border-bottom-colors: none;
  -moz-border-left-colors: none;
  border-left-colors: none;
  border-image-source: none;
  border-image-slice: 100% 100% 100% 100%;
  border-image-width: 1 1 1 1;
  border-image-outset: 0 0 0 0;
  border-image-repeat: stretch stretch;
  padding-top: 0.5em;
  padding-right: 0.5em;
  padding-bottom: 0.5em;
  padding-left: 0.5em;
}

th {
  font-weight: bold;
  text-align: center;
}

caption {
  margin-bottom: 0.5em;
  text-align: center;
}

p, fieldset, table, pre {
  margin-bottom: 1em;
}

input[type="text"], input[type="password"], textarea {
  width: 12.25em;
}

.navbar {
  background-color: black;
  color: white;
  font-size: smaller;
}

.Pagetitle {
  font-size: large;
  font-weight: bold;
}

.navbar:hover {
  font-weight: normal;
}

#downloads:hover {
  font-weight: normal !important;
  font-size: smaller !important;
}

.contact:hover {
  font-weight: bolder;
}

.downloads:hover {
  font-weight: bolder;
}

.store:hover {
  font-weight: bolder;
}

.downloads {
  font-weight: normal;
}

.store {
  font-weight: normal;
}

.contact {
  font-weight: normal;
}

.versionnum {
  font-size: large;
  color: black;
  font-weight: bold;
}

.releasedate {
  font-size: small;
  font-style: italic;
  color: black;
}

.releasecontent {
  font-size: medium;
}

.modrev {
  font-style: normal;
  font-weight: normal;
  font-size: small;
  color: #3333ff;
}

.selectrev {
  font-weight: normal;
  font-style: normal;
  color: #3333ff;
  font-size: small;
}

.yui-u {
  font-size: small;
}

.backhome {
  font-size: smaller;
}

.latestrev {
  font-size: smaller;
}

.back {
  font-size: small;
}  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  


Modular Firmware Revision History

[go
                back to support home](EN_EUGENE_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Eugene
                release notes.  

              ](EN_EUGENE_RELEASE_NOTES.md)

[Eugene
                changelog history.](EN_EUGENE_PREVIOUS.md)

[Select
                firmware changelog history.](EN_SelFW.md)  
  
  
  
  
Modular_1.085  
Release
                  2021-Apr-23
- Added two new European CAN ABS modes for RX8
- Changed closed loop fuel condition to Load1 instead of IMAP
- Added support for the LS2 trigger to support 4 channels of the
                2-Long 2-Short cam triggers
- Improved ignition output codeModular_1.084  
Release
                  2020-Nov-16
- Turbo timer improved.
- Added cranking RPM in the condition for thermofan to turn ON.
- First cut of rev matching auto blipping on downshift.
- Added JDM RX8 ABS modes.  
Modular_1.082  
Release
                  2020-Aug-14
- Allowed inversion of alternator loadModular_1.081  
Release
                  2020-Jul-31  

- Changed missing tooth cam trigger on BMW S54 to CAS3.
- Corrected ignition output sense during ignition output test.
- Changed S54 exhaust cam range from -22.5 -> 67.5 instead
                to -67.5 -> 22.5
- Improved communications reliability of Haltech TCA2.
- Added support for S54 BMW exhaust VVT (VANOS).
- Changed max temperature voltage from 4.5V to 4.7V, if you
                have a voltage table (ie external
- Changed Rover back to reluctor for trigger 1 and user defined
                for triggers 2 and up.
- Fixed problem with temperature reading when set to a
                non-temperature input channel as the voltage source.
- Changed Rover trigger so it only looks at the falling edge in
                reluctor or hall effect mode on the cam trigger.Modular_1.075  
Release
                  2020-Jun-15  

- Changed single missing tooth threshold to plain 1.5 instead of
                needing to be <1.25 or >1.75
- Corrected "set crank period" for Rover trigger mode  
Modular_1.073  
Release
                  2020-May-20  

- Fixed JC20B ignition mode not using split table.Modular_1.072  
Release
                  2020-Apr-17  

- Added initialisation for closed loop boost
- Added user temp #1 to output fuel level on Haltech V2 CAN
                protocol
- Corrected fuel pressure reading on Haltech V1 protocolModular_1.070  
Release
                  2020-Mar-07  

- Added early Lotus / Rover K trigger type 36-1-1-1
- Added interrupt delatching on trigger inputs (improves
                stability with certain trigger types)
- Added BMW VANOS outputs
- Fixed scaling on EGT outputs on Haltech CAN
- Added fixed rising edge trigger on CAS 4/5 frequency
                measurement on Subaru magic edge switching mode
- Changed pulse ignition output test to handle inverted ignition
                output conditions
- Added RX8 EU ABS Mode 2 compatibility.  
Modular_1.063  
Release
                  2019-Aug-19
- Added trigger type for BEAMS dual VVT (already supported
                through generic mode).

Modular_1.062  
Release
                    2019-Aug-06
- Changed ignition timing air temp correction not to be applied
                at idle (coolant temp still is). Added pressure ratio load
                source to VVT.
- Added battery voltage PID to OBD2.
- Changed VSS calc to unsigned.
- Changes to settings caching code (min main loop speed now 600
                Hz).
- Added blanking on aux output 4 for GM stepper motors.
- Added Honda Aquatrax.
- Changed Haltech CAN wideband so that free air shows lambda
                10.000 instead of an error. Changed fuel diff pressure
                measurement so it uses the IMAP value rather than IMAP
                overridden by predicted MAP value.
- Fixed ignition output overcurrent bug - even when disabled it
                was tripping on the ignition outputs because it was reading the
                wrong index in the field.
- Added over MAP fuel temperature latching for flex sensor.
- Fixed bug introduced in CAN UK RX8 ABS module.
- Added CAN output for UK model RX8.  
  
Modular_1.050  
Release
                  2019-May-05
- Added overcurrent protection for large output module on aux
                output and injector output pins.
- Adding support for Grand National plugin ECU.

Modular_1.046  
Release
                    2019-Feb-25  

- Added digital logic inputs (able to trigger a digital input
                from a channel being < or > a constant).
- 2 predefined aftermarket triggers with Hall effect sensors
                were set as reluctor, set now to digital.Modular_1.042  
Release
                  2019-Jan-22
- Added support for E85 separate target lambda tables.  
Modular_1.041  
Release
                  2019-Jan-15
- Added support for vehicle speed as boost speed axis instead of
                RPM.
- Changed minimum boost function clipping to current baro
                pressure so it doesn't happen in open loop duty cycle mode.
- Changed Haltech CAN ethanol percentage output scaling.
- Added native support for Buick 18/3/1 trigger (V6).
- Added support for Haltech TC8.
- Changed RX8 CAN to always send full packet.
- Locked duty cycle override of DBW to 1 kHz frequency.
- Changed boost control behaviour to calculate target boost all
                the time, not only when in boost conditions.
- Changed boost control target calculation so that the minimum
                target is the barometric pressure.
- Removed 4ec from RX8 CAN output.  
  
  
  
Modular_1.035  
Release
                  2018-Nov-13  

- Moved Safeties to different bits to support SW changes.
- Added 20B ignition mode.
- Removed ignition cut on multiplexed ignition outputs.Modular_1.032  
Release
                  2018-Nov-07
- Remove requirement for Motec PLM to be in RUN mode, so that it
                also works for the LTC.
- Added support for internal lambda module.
- Made RX8 CAN US ABS an option.
- Added support for fixed digital inputs on RX8 V2.
- Added support for internal wideband module.
- Changed RX8 CAN output for US models.
- Removed injection limit on duration for final stage.
- Added ability to use channel thresholds for digital inputs.Modular_1.027  
Release
                  2018-Oct-22  

- Added delay option for oil pressure.
- Added delay for ignition outputs
                  after starting.
- First prototype of internal wideband
                  lambda.
- Changes to RX8 CAN for US ABS unit.
- Changes to ECU locking to make more
                  secure with earlier firmware.
- Changes to gains of adaptive fuel to
                  improve stability.
- Changes to ECU locking to store in
                  external MRAM as well as flash.
- Enabled adaptive fuel.
- Moved memory map around.
- Changed handshaking of injector test
                  code to improve comms reliability.
- Added password locking function
                  (still beta).
- Fixed ignition PWM output frequency.
- Fixed injector / ignition test
                  function.  
Modular_1.015  
Release 2018-Sep-10  

- Removed wait for flash readiness after writing block - to
                avoid lockup (and misfire).
- Fixed target boost mode.  
Modular_1.013  
Release 2018-Sep-03  

- Added S660 trigger support.
- Added USB engine reset (if engine is stopped).
- Fixed aux 5 dropout if engine stopped on M1200.
- Added support for Haltech TCA box.Modular_1.011  
Release 2018-Aug-17  

- Improvements to transient ignition timing.Modular_1.010  
Release 2018-Aug-09  

- Update for new RX8 VB ID.
- Added support for ECU Master EGT CAN.
- Added support for Daihatsu 3+1 on cam.
- Added trigger error detection on Evo trigger.Modular_1.007  
Release 2018-Jul-26  

- Added support for MAP on single cylinder engines
                for 720 degree reset.
- Added support for single tooth per 360 degrees
                (single tooth on the crank).  
  
Modular_1.005  
Release 2018-Jul-09  

- Changed trigger on both edges generic mode.
- Changed Subaru EZ36 (broken in 0.243).Modular_1.004  
Release 2018-Jun-20  

- Added variable launch control addition
- Added Mazda FSDE trigger
- Fixed bug with arbitrary scaling of
                temperature inputs (introduced in 0.254)
- Added 5V monitoring of mini analogue board
- Changed base angle of Holden V8 trigger.Modular_0.255  
Release 2018-Jun-13  

- Cruise voltages for Subaru.
- Arb temp calibrations, plus re-enabled
                boost locking for learning table
- Fuel volume calculation update - test using
                RPM output on AEM as fuel used (in 1/100 L). Added in more
                injector models (85 - 92).
- Fixed key-on time dependent variables
                (sometimes stepper timer would latch up).
- Changed interrupt handling on m1200
                ignition outputs to improve ignition timing accuracy at very low
                RPM on low tooth count engines.
- Changed timing interrupt priority on M1200
                ignition outputs (to improve timing accuracy on M1200).Modular_0.249  
Release 2018-May-28  

- Changed extra tooth threshold on Honda
                trigger.
- Added CAN TRC LED for RX8 based on DSC
                input (still experimental).
- Added arbitrary pressire sensor
                configuration.
- Subaru 4 x VVT updateModular_0.245  
Release 2018-May-17  

- Added Purge Valve function.Modular_0.243  
Release 2018-May-15  

- Added QR25 trigger.
- Fixed separate banks 1st half / 2nd half
                dual lambda reading averaging within a bank.
- Holden V8 VP / VT trigger code.
- DBW TRC code.
- Changed CAN snoop so on RX8 mode it uses
                channel 2.
- Fixed Innovate serial input lean reading
                introduced in 0.233.Modular_0.237  
Release 2018-Apr-24  

- Changed closed loop idle to only go to
                closed loop idle if VSS=0 when VSS is enabled.
- M2000 optimised ignition output for FC
                igntion.
- M1200 timing change.
- User log variable channels for internal log
                (fix).
- Added input for Innovate to read full lean
                when it's just showing O2.
- Changed Nissan trigger 6 cyl dizzy edge
                sensitivity.
- Added tps delta trans fuel mode.
- First cut at traction code.
- Added 5 cylinder output mode on M1200.
- Improved ignition outputs on low tooth
                count trigger engines.
- Added idle to close at crank option.
- Added EGT2 on Racepak output.
- Optimised internal logging (faster
                operation).Modular_0.220  
Release 2018-Mar-12  

- Moved temperature sensors into models
                module.
- Added option for constant pullup value of
                1k on temperature inputs (setting).
- Added more injector options.
- Another attempt for Subaru switching WFs.
- Added VQ25, VH45 and Jazz triggers.
- Added VQ30 trigger.
- Added 4+1 Suzuki trigger, Audi 5 cyl dizzy.
- Changed ignition timing idle mode so it
                does it on IDLE_DERIV in absolute RPM mode, and CLOSED_IDLE in
                RPM error mode.Modular_0.214  
Release 2018-Feb-28  

- Partial coding of new triggers. Changed
                closed loop fuel correction time.  
Modular_0.212  
Release 2018-Feb-22  

- Added Gaugeart comms.
- Subaru changing phases code.
- Internal logging changes.  
Modular_0.209  
Release 2018-Jan-22  

- Added additional call to Angtrack_Stopped
                to better handle the case when engine is already running when
                ECU is powered up with certain triggers (esp. Subaru 36-2-2-2).
- 2nd cut of Subaru 6/7 trigger mode.
- Added -3, -6, -9 dB headphone settings.
- Added Idle closed loop status output.
- Added Subaru 6/7 trigger mode.  
Modular_0.205  
Release 2018-Jan-15  

- Updated version of internal logging code.
- Added RX8 odometer.
- Added Suzuki G13B / GTi.
- Enabled logging in the code (disabled by
                default).
- Added ability to invert ignition outputs
                for MSD, Honda... that's about
                it.
- ***Note that on an M1200 because of the
                hardware current limiting you'll still need to either bypass the
                internal resistor or use the normal output mode (falling edge)
                and an external ignitor.
- Subaru EJ25 trigger version 5.
- Subaru EZ36 trigger version 2.
- Subaru EZ36 trigger version 2.
- Changed Honda K to 30 degrees retarded.
- Honda S2000 AP1, AP2, K20A / K24A trigger
                V1.
- Ford V8 trigger V4.
- Ford V8 trigger V3.
- Happy New Year!Modular_0.194  
Release 2017-Dec-07  

- Ford V8 trigger V2
- Ford V8 trigger V1
- 5th iteration of EJ25 code
- 4th iteration of Subaru edge sensitivity
                code (22.5 degree window, ignore edges during the missing tooth
                gap). Also coded 30 degree window for Subaru EZ36, seems to have
                stable timing on bench with inverting triggers.
- Support for 3 cylinder, single pulse per
                cylinder code.
- 3rd iteration of Subaru edge sensitivity
                code (22.5 degree window).  
Modular_0.189  
Release 2017-Dec-05  

- 2nd iteration of Subaru edge sensitivity
                code.
- Changed subaru edge sensitivity for Subaru
                magic polarity changing sensors.
- Fixed DBW problem introduced with dyno code
                disable.
- Added first version GaugeArt output code.
- Changed Lotus type 1 CAN output for
                odometer reading correctly.Modular_0.185  
Release 2017-Nov-24  

- Added Lotus type 2 CAN odometer function
- Added filtering on injector test
- Implemented Lotus type 2 CAN output coding
- Implemented fixed time air shifter output
- Implemented Lotus type 1 CAN output coding
- Implemented DSC input on RX8Modular_0.181  
Release 2017-Nov-20  

- "Muted" injection outputs until outputs
                synchronised.
- Implemented OBD data reading.
- Added ability for single pulse per TDC
                trigger.
- Added bootloader updating code to force
                update to M1200 bootloader if it's an M1200 application code.
- Implemented injector / ignition of M1200,
                Increased closed loop MOP target tolerance to 3.5 and slowed
                down movement when it gets close.
- Thermofan disable for first second after
                starting to allow filtered temperatures to stabilise. Increased
                closed loop MOP target tolerance to 3%.
- RX8 CAN code.  
Modular_0.174  
Release 2017-Oct-30  

- "Muted" injection outputs until outputs
                synchronised.  
Modular_0.173  
Release 2017-Oct-27  

- Added K6A trigger non-VVT
- Throttle blip code, gradual ign retard
                re-instate
- Strain gauge code
- Added Holley CAN output - not full speed
                yet
- MX5 NA ignition output glitch at specific
                RPM on M1200 solved.  
Modular_0.169  
Release 2017-Oct-18  

- Added 4G69 trigger
- Changed EZ36 trigger base back to 30 BTDC
- Added / fixed Mitsubishi 6+1
- Added Suzuki Alto / RS Swift triggers
- Added Suzuki Swift Gen 5 trigger
- Changed M1200 startup sequence
- Daihatsu Mira trigger and increase Max 0-5V
                input to 5.3V  
Modular_0.162  
Release 2017-Oct-10  

- Subaru EZ36; automatically detect either
                edge on all 4.
- Output enable set high by bootloader
                (modular) and pulled low after initialising comms., to help with
                S15 etc ECUs.
- Subaru 2 x VVT update for all reluctors.
- Trigger change for 2 x VVT Toyota.
- Added 4 cyl Mitsu / Mazda trigger.
- Added support for O2 voltage switching in
                V07 HW.
- Added support for turbo speed inputs up to
                6550 Hz (224 k RPM on 14 tooth BW).
- Sped up low level input updating for use
                with built-in scope.
- Changed min time for 2 missing teeth to
                2.125 instead of 2.5 to be more forgiving of double-2-missing
                teeth on Subaru engines.
- Changed Subaru base angle to 35 degrees
                instead of 30.
- Added variable headphone gain and knock
                gain.
- Added CAN snooping function.
- Changed RX8 base angle.
- VE DC motor coding.  
Modular_0.148  
Release 2017-Aug-24  

- Subaru EZ36 automatically detect either
                edge.  
Modular_0.147  
Release 2017-Aug-22  

- Some changes to Adaptronic native mode,
                added VSS / gear / MGP.  
Modular_0.145  
Release 2017-Aug-11  

- Changed injector 3 output pin on M1200.
- Inverted sign of VVT inputs on RT Mini
                input board for quad VVT engines.
- Implemented proper scaling of frequecy /
                period on RT Mini inputs.
- Added Adaptronic native CAN mode.  
Modular_0.141  
Release 2017-Aug-08  

- Added option for fuel temp sensor type to
                be -2 -> read from flex (rather than having to choose in
                source).
- Added VNET remap option.
- RColt trigger
- Native Racepak / VNET CAN output
- Haltech V1 CAN output
- Haltech V2 CAN output - untested
- Motec PLM implementation.
- Built-in diagnostics for output module.
- Start of CAN implementation.Modular_0.136  
Release 2017-Jul-20  

- RColt triger implementation.
- Disabled "always allow async" option.
- Added allowance of single edge Nissan angle
                error.
- Changed module address reading for output
                module to happen once at startup instead of every time through
                main loop (noise immunity).
- Ignition output bias override update for
                firmware test.Modular_0.133  
Release 2017-Jul-14  

- Big changes for USB comms
- Disabled 16 MB flash device
- Added "write to block 0" to have same
                function as write to block 513
- Sped up USB comms for faster recognition by
                Windows
- Added FAT, root dir and FAT-16 filesystem
                so Windows doesn't keep saying "format this!"
- Added indirect write (to block 1) to effect
                a write to any block
- Corresponding changes in AdapComm.DLL
- Also has a new bootloader updater, so when
                you load in this firmware, it also checks the bootloader and
                updates it if required.Modular_0.129  
Release 2017-Jun-30  

- Added more injector models
- Added Zeitronix input, AEM input, PLX
                output
- Added debugging for async calculations
- Adding minimum injector duration of 0.2ms
                for manual async
- Temperature input bias algorithm change
- Changed ADC timing also to increase
                accuracy of current measurement of injector outputs on M1200
- Added Subaru 36-2-2-2 trigger modes
- Added Subaru EZ36 trigger mode
- M1200 low level output scope, M1200 memory
                fix
- M1200 compatibility version.Modular_0.121  
Release 2017-Jun-16  

- Implemented open loop MOP control option
                for FC / FD / FE MOPs, and closed loop FE MOP.
- Implemented short pulse function on ID
                injectors  
Modular_0.119  
Release 2017-Jun-09  

- Added M1200 compatibility.
- Changed I2C initialization so it only
                happens with 12V power, to speed up USB initialisation.
- Added turbine speed calculation.
- Added alternate pinout for MX5 NB ECUs.
- Added voltage tolerance option for gear
                detection.Modular_0.116  
Release 2017-Jun-02  

- Reduced min time to fire for slowed down
                outputs to improve ignition pulse accuracy at high RPM.Modular_0.115  
Release 2017-May-23  

- Flipped NB MX5 trigger by 360 degrees
- Added dedicated RX7 and RX8 triggers (std
                RX7 and FFE models)
- Changed angle detection / wasted spark / DF
                ignition output logic
- Slowed down timers in output module by
                factor of 4 to improve low RPM performance
- Implemented injector models  
Modular_0.110  
Release 2017-May-05  

- Increased dead time on aux drive high PWM
                outputs
- Changed DBW target TPS scaling / algorithm
- Verified NB MX5 trigger
- Fixed ms cranking mode
- Added V8 Audi trigger
- Fixed minimum pulsewidth for async pulses
                (introduced in 0.105).Modular_0.108  
Release 2017-May-01  

- added V8 Audi trigger (needs software
                update)
- fixed minimum pulsewidth for async pulse
- Knock windowing, knock retard / recovery
- Made I2C reset conditions more strict
- Thermofan delay implementation
- Added minimum effective PW and minimum fuel
                volume
- Added MGP as tuning option
- Increased aircon switch filter to 500ms
- Implemented knock time domain and angle
                domain live views
- Fixed trigger / logic on built-in scope
- Disabled CAS3 as trigger input when used
                for flex
- Added phantom vehicle board numbers for S13
                -> S15 and S14 -> S13 CA18DET.Modular_0.101  
Release 2017-Mar-30  

- Added FC ignition output
- Changed flat shift to check history of gear
                selection before closed loop flat shift
- Changed ana gear input to detect neutral
                correctly
- Found & fixed PWM bug on injector
                outputs
- Found & fixed PWM race on injector/aux
                outputs
- Changed BEAMS temp calibration and trigger
- Changed flash writing state to introduce
                wait for BSY (settings cache)
- Added Toyota BEAMS coolant temp sensor
- Fixed generic temp sensor calibration
- Extended range of built-in temp
                calivrations to 150°C
- Changed some names of variables to be more
                intuitive
- Added injector duty cycle and fuel usage
                calculations
- Changed VVT to only show channels in use on
                main gauges window
- Added visibility for resistance calculation
                for temperature inputs
- Added visibility for MGP (and MGP2 on dual
                bank engines)
- Added new coolant temperature type - defi
- Changed oil pressure safety to work down to
                zero RPM
- Fixed arbitrary temperature cal
- Added option for idle ignition timing table
                to be independent (not based off main ignition map)
- Updated AIM output so it gives gear + 1...
                to read correctly on dash
- Evo 4-9 trigger
- Added FW VSS filter, analogue gear
                detection, closed loop ignition cut
- Slowed down RT output so as not to overload
                the dash
- Changed individual fuel trim TPS to be 0.1%
                resolution
- Added mini analogue-input supportModular_0.087  
Release 2017-Mar-9  

- DBW to report motor current
- Added ability to select fuel / oil pressure
                from alternate sources
- USB MSD changes
- Check for high RPM Nissan operation (no
                code change)
- Fixed decel CEL light
- Implemented antilagModular_0.082  
Release 2017-Feb-22  

- Delay for cut reason, so it's persistent in
                logs
- Delay for async so it goes to zero after
                the async is done
- Leanout delay
- Handle negative fuel delivery values
- Added launch enable / in launch annuciators
- Added ignition test
- fixed closed loop idle enable bug
- Made launch control data match latest SW  
Modular_0.076  
Released 2017-Feb-08  

- Added diagnostics for mini aux output
                module
- Added mini aux output module support
- Added more DBW functionality
- Added firmware security for other modules
- Changed TPS / EGT output calibration for
                AIM dash
- Added 4 x VSS, quad VVT cam support + 2GRFE
                trigger dedicated mode  
Modular_0.073  
Released 2017-Jan-25  

- Changed ignition with 15 degree trigger
                angle
- Found & fixed ignition output cut
                showing 100% during overrun.  
  
  
©2020
        Adaptronic  
