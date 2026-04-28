Metering Oil Pump Control on Mazda Rotary Engines with Modular ECUs/*

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
  font-size: medium;
}

.backhome {
  font-size: smaller;
}

.latestrev {
  font-size: smaller;
}

.bodytxt1 {
  font-size: xx-small;
}  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  


Metering Oil Pump Control on Mazda Rotary
              Engines with Modular ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[  

              ](EN_EUGENE_ABOUT.md)

[  

              ](EN_EUGENE_KBSC_TG.md)

  


[  

              ](EN_SelFW.md)

  


  
  
  
  
  
In this article we’ll discuss how to
                  set up the metering oil pump on the RX7 13B engines.  
  
First of all, let’s discuss the function of the metering oil
                  pump, MOP or oil metering pump, OMP (Mazda use the two terms
                  interchangeably in different documents). It’s a mechanical
                  device which allowed pressurised oil to be fed from the oil
                  system to be fed into the rotor housings in the inlet area.
                  It’s driven by a stepper motor, whose position determines the
                  amount of oil that gets injected. There’s also a position
                  feedback sensor on the pump that measures the position of the
                  pump, and the ECU controls the stepper motor to achieve a
                  certain position reading on the feedback sensor. This article
                  does not cover the oil metering on the series 1 and series 2
                  RX8 engines, both of which are different from the RX7 engines,
                  and also different from each other.  
  
  
![OMP_parts](../images/021_MOP/OMP_parts.png)  
  
Oil Metering Pump of RX7 13B  
  
The connections to the pump are as follows.  
  
There is a 6 wire stepper motor which drives back and forward
                  to control the amount of oil delivered. Like other 6 wire
                  stepper motors, the middle pin on each row is 12V power and
                  the two pins other side must be driven in opposite phases. So
                  you will need an output for each of the 4 drive pins on the
                  motor, that is an ignition, injector or auxiliary output. On
                  the plug and play ECUs, only 2 ignition outputs are used to
                  drive the motor directly, with the opposite phases generated
                  by an additional circuit in the ECU. This allows you to run
                  the motor using only 2 outputs out of the 20 available rather
                  than 4.  
  
![Plugandplayconnection](../images/021_MOP/Plugandplayconnection.png)  
  
![Wireinconnection](../images/021_MOP/Wireinconnection.png)  
  
On the sensor side, the device is a 3 wire potentiometer,
                  similar to a TPS, so the sensor needs sensor ground, 5V supply
                  and a signal connection. By default the ECU will use the servo
                  input, but you can use any 0-5V input on the ECU for the MOP
                  position feedback input. This is all handled in the factory
                  wiring of a plug and play ECU anyway.  
  
![Sensorconn](../images/021_MOP/Sensorconn.png)  
  
Let’s discuss the settings required for the MOP to work.
                  Firstly,   you need to select the input channel
                  for the position sensor, ie where you have wired the position
                  sensor to. If you select “default” then the ECU will assume
                  it’s wired to the servo input, which is how it’s configured on
                  the plug-in ECUs.  
  
  
![Source](../images/021_MOP/Source.PNG)  
  
Source set to default  
  
In terms of outputs, if you’re using a plug-in ECU which
                  already has the circuitry to drive the other two phases, you
                  need to select one of these outputs as MOP step A, and the
                  other as MOP step B. Configure them as PWM at 1 kHz for
                  reasons I’ll explain a bit later.  
  
![MOPA](../images/021_MOP/MOPA.PNG)  
  
![MOPB](../images/021_MOP/MOPB.PNG)  
  
If you don’t have extra hardware to drive the boards then you
                  need to set the other two outputs to be metering oil pump
                  step A inverted and metering oil pump step B inverted,
                  both are PWM enabled at 1kHz.  
  
![MOPBinv](../images/021_MOP/MOPBinv.PNG)  
  
![MOPAinv](../images/021_MOP/MOPAinv.PNG)  
  
The final setting is the target MOP table, which is a function
                  of RPM and manifold pressure. This table has been calculated
                  by monitoring the behaviour of the factory ECU on the series 5
                  and series 6 engines; I understand that different types of
                  seals have different oiling requirements so you may need to
                  premix as well, please consult your engine builder or seal
                  supplier if you’re unsure. The factory behaviour is that the
                  amount of oil injected increases with RPM and with MAP, in
                  other words it’s roughly related to the fuel quantity
                  delivered, which also makes sense intuitively because people
                  use premix.  
  
![targettable1](../images/021_MOP/targettable1.png)  
  
![targettable](../images/021_MOP/targettable.png)  
  
Now, let’s discuss how to check that it’s working correctly.
                  The ECU will chase the target value by driving the stepper
                  motor outputs. If it drives for a long time and ends up in the
                  wrong direction, it switches the outputs around and tries to
                  go the other way. When the ECU is driving the motor forwards
                  and backwards, the outputs are driving high and low
                  alternately, so you will see the MOP step A and B numbers
                  flicking between 0 and 100%. This happens too fast to be able
                  to see the individual steps in a PC based log, but you can see
                  them using the built-in scope or a real scope.  
  
![Scopestep](../images/021_MOP/Scopestep.png)  
  
When the ECU gets to within a small error band of the target,
                  it drives both outputs with a 50% duty cycle. This uses the
                  coil inductance to reduce heating in the motor windings,
                  compared to leaving one coil energized the whole time. So when
                  it’s at the target you should see 50% on both outputs. If it
                  happens to move either side of the target, it will take a step
                  back or forward as required.  
  
Let’s discuss how to diagnose a problem with the MOP. The most
                  likely problem, based on the support questions we get, if the
                  ECU configuration is correct, is going to be wiring. So
                  firstly check the basics, ie:  
  
![Wireinconnectioncopy](../images/021_MOP/Wireinconnectioncopy.png)  

-   
The two motor +12V pins have 12V on them  
  
![TestSensor](../images/021_MOP/TestSensor.png)  

-   
The sensor has 5V at one side and 0V at the other  
  
![SensorWiring](../images/021_MOP/SensorWiring.png)  

-   
The sense wire is connected through to the input on the
                        ECU – for example when you short it to 5V, you can see
                        the input change to 5V on the F11 ECU data screen  
  
Firstly go to the outputs page and select Outputs 13 and 14 as
                  being “none” rather than “MOP”. Follow the following tables to
                  check the voltages (on the different models):  
  
First test: Both outputs set to none:  
  
![1&2None](../images/021_MOP/1&2None.png)  
  
  
  
  
Series
                          5 ECUSeries
                          6 ECUSeries
                          8 ECUVoltage  
  
(approx)  
Internal
                          connectionECU
                          pinECU
                          pinECU
                          pinWire
                          colWire
                          colWire
                          col4TB
                          / L4JB
                          / L1WB
                          / L12VIgn
                          5 (op 13)4VB
                          / R4LB
                          / Y1AEB
                          / Y0VIgn
                          5 invert4SB
                          / Or4IB
                          / Or1SB
                          / Or12VIgn
                          6 (op 14)4UB
                          / G4KB
                          / Lg1AAB
                          / Lg0VIgn
                          6 invert  
  
Second test: Set output 13 to “none, invert”  
  
![1inv&2](../images/021_MOP/1inv&2.png)  
  
Series
                          5 ECUSeries
                          6 ECUSeries
                          8 ECUVoltage  
  
(approx)  
Internal
                          connectionECU
                          pinECU
                          pinECU
                          pinWire
                          colWire
                          colWire
                          col4TB
                          / L4JB
                          / L1WB
                          / L0VIgn
                          5 (op 13)4VB
                          / R4LB
                          / Y1AEB
                          / Y12VIgn
                          5 invert4SB
                          / Or4IB
                          / Or1SB
                          / Or12VIgn
                          6 (op 14)4UB
                          / G4KB
                          / Lg1AAB
                          / Lg0VIgn
                          6 invert  
  
Third test: Put output 13 back to “none”, set output 14 to
                  “none, invert”  
  
![1&2inv](../images/021_MOP/1&2inv.png)  
  
Series
                          5 ECUSeries
                          6 ECUSeries
                          8 ECUVoltage  
  
(approx)  
Internal
                          connectionECU
                          pinECU
                          pinECU
                          pinWire
                          colWire
                          colWire
                          col4TB
                          / L4JB
                          / L1WB
                          / L12VIgn
                          5 (op 13)4VB
                          / R4LB
                          / Y1AEB
                          / Y0VIgn
                          5 invert4SB
                          / Or4IB
                          / Or1SB
                          / Or0VIgn
                          6 (op 14)4UB
                          / G4KB
                          / Lg1AAB
                          / Lg12VIgn
                          6 invert  
If an output always shows 0V, then that normally means that
                  there is an open circuit coil in the pump motor, or that
                  there’s a disconnection between the motor and the ECU (for
                  example a broken wire or a bad connection).  
  
Finally, put the settings back to their standard values
                  (output 13 = Metering Oil pump Step B, output 14 = Metering
                  Oil Pump Step A).  
  
![orig](../images/021_MOP/orig.png)  
  
If all of those pass, then the ECU is driving the outputs
                  correctly, so the next step would be to check the pump itself,
                  for open circuit windings or mechanical problems.  
  
Additional information when using wire-in ECUs.  
  
Make sure to follow the diagram below when wiring the oil
                  metering pump on RX7 FCs and FDs .  
  
![MOPwirein](../images/021_MOP/MOPwirein.png)  
  
  
![FDMOPwirein](../images/021_MOP/FDMOPwirein.png)Next
                  configure either auxiliary, ignition or injector outputs to
                  drive your motor. In this example let’s use auxiliary outputs.
                  Select output 17 and 18 and configure it as “Metering Oil Pump
                  Step A” and “Metering Oil Pump Step B”, both should be
                  set as PWM at 1kHz. Then select output 19 and 20 as 
                  “Metering Oil Pump Step A, inverted” and “Metering Oil
                  Pump Step B, inverted”, both should also be set as PWM at
                  1kHz.  
  
![Sampleoutput](../images/021_MOP/Sampleoutput.PNG)  
Thank you and happy learning!  
©2018
        Adaptronic  
