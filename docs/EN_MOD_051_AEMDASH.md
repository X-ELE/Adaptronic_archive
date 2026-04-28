Setting up the AEM CD7 Dash with the Adaptronic Modular ECU/*

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
  


Setting up the AEM CD7 Dash with the Adaptronic
              Modular ECU

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Using
                a Racepack IQ3 Dash](EN_MOD_049_RACEPAK_VNET.md)[ ](EN_EUGENE_ABOUT.md)

[CAN
                Protocol and the Adaptronic CAN System  

              ](EN_MOD_050_NATIVECAN.md)

  


[  

              ](EN_SelFW.md)

  


  
  
  
  
  
The AEM CD7 dash is one of the many
                  full colour TFT dashes on the market. It has built in support
                  for many aftermarket ECUs and a fully configurable CAN system.
                  This article shows two ways that it can be used.  
  
In both, we will just use the CAN1 connection on the
                  dash. The dash actually has 2 CAN busses, but we will just use
                  the first one in this example.  
  
In terms of physical connection, all the pins we
                  need are found on the 4 pin DTM connector. The colours are as
                  follows:  
  
Pin and Colour  
  
AEM Name  
  
Our connection  
  
1 - White  
  
CAN 1+  
  
CAN H – J2-15 on M2000 /
                            M6000  
  
2 – Green  
  
CAN 1-  
  
CAN L – J2-23 on M2000 /
                            M6000  
  
3 – Red  
  
Switched Power  
  
Ignition  switched
                            power - J2-7 on M2000 / M6000  
  
4 – Black  
  
Power ground  
  
Power ground – J2-8 on
                            M2000 / M6000  
  
![1_wire](../images/051_AEM_Dash/1_wire.jpg)  
  
Note that here, the standard red/black are used for
                  power and ground, and white/green are the CAN pair, unlike the
                  Racepak where they use red/green for power and ground, and
                  white/black for the CAN pair. The best thing about standards
                  is that there are so many to choose from.  
  
Using the Haltech V2 Protocol  
  
The first method is to use the Haltech V2 protocol.
                  The Adaptronic Modular ECUs can emulate the Haltech V2
                  protocol which allows it to be used with any dash that
                  supports the Haltech, with the exception of the Haltech IQ3
                  simplicita, but if you want to use that dash, then please read
                  the article or watch the video on how to use the Racepak
                  dashes.  
  
Firstly, the Haltech protocol specifies a bit rate
                  of 1 Mbps, but both the ECU and the dash allow you to choose
                  different bit rates. So to be correct, the ECU should be set
                  to 1 Mbps, and the termination should be set to “on”. If
                  you’re using the secondary CAN port on a Modular ECU that
                  supports a second CAN port, the termination is always on and
                  can’t be disabled.  
  
Secondly, the dash must be configured using the AEM
                  Dash Design software. To do this, load your dash configuration
                  and then go to Setup -> Display.  
  
![2_AEM_1_SetupLocation](../images/051_AEM_Dash/2_AEM_1_SetupLocation.png)  
  
In the Setup editor, go to CAN Receive.  
  
![3_AEM_2_CanReceive](../images/051_AEM_Dash/3_AEM_2_CanReceive.png)  
  
Select the following settings:  

- Choose port 1 (because we are connecting via
                      the CAN1 port on the 4-pin DTM connector)
- Baudrate = 1 Mbps (default is 500 kbps)
- Termination resistor = checked / enabled
- Port mode = normal
- Motec M800 support =off  
![4_AEM_3_CanReceive_1Mbps.png](../images/051_AEM_Dash/4_AEM_3_CanReceive_1Mbps.png)  
  
Then select the “Import CAN…” button  
  
![5_AEM_4_import_can](../images/051_AEM_Dash/5_AEM_4_import_can.png)  
  
Select the Haltech V2 AEMCAN template:  
  
![6_AEM_5_Haltech_V2_selection](../images/051_AEM_Dash/6_AEM_5_Haltech_V2_selection.png)  
  
And select “replace” when it asks you if you want to
                  override the new channels.  
  
Send this to the dash using the “Upload to Display”
                  or Ctrl+U and the two devices will now talk to eachother.  
  
The following lists the Haltech channels as
                  implemented in Modular firmware 0.145 and notes for them. Note
                  that the full CAN spec is Haltech’s intellectual property, so
                  if you want a full description of Haltech’s protocol, please
                  do not ask us. This is just to describe individual channels,
                  which ones are available and anything weird or unusual with
                  how it is interpreted by the AEM dash:  
  
Haltech
                              name  
  
Our
                              name  
  
AEM
                              dash name  
  
Notes  
  
RPM  
  
RPM  
  
Engine
                            Speed  
  
  
  
Manifold
                            Pressure  
  
IMAP  
  
Boost  
  
Haltech
                            defines it as absolute pressure (as we do), and
                            that’s what we send, but it’s displayed as “boost”
                            on the dash. Eg 56 kPaA, shows up on the “boost”
                            channel on the dash as 56 kPa, which is misleading.  
  
Throttle
                            Position  
  
TPS
                            overall  
  
Throttle  
  
  
  
Fuel
                            Pressure  
  
Fuel P  
  
  
  
This is
                            given as offset from 101.3 kPa (absolute pressure
                            assuming baro = 101.3 kPa). We add 101.3 when
                            outputting on this channel because we measure oil
                            pressure as a gauge pressure. It displays correctly
                            on the dash.  
  
Oil
                            Pressure  
  
Oil P  
  
Oil Press  
  
See Fuel
                            Pressure  
  
Engine
                            Demand  
  
Load
                            Value 1  
  
  
  
We output
                            this, but I’m not sure which channel it is mapped to
                            on the AEM system  
  
Injection
                            Stage 1 Duty Cycle  
  
Injector
                            1 Duty  
  
  
  
  
  
Injection
                            Stage 2 Duty Cycle  
  
Injector
                            “n+1” Duty  (where “n” is number of cylinders)  
  
  
  
  
  
Injection
                            Stage 3 Duty Cycle  
  
Injector
                            “2n+1” Duty  
  
  
  
  
  
Injection
                            Stage 4 Duty Cycle  
  
Injector
                            “3n+1” Duty  
  
  
  
  
  
Ignition
                            Angle (Leading)  
  
Ignition
                            timing  
  
  
  
  
  
Wheel
                            Slip  
  
  
  
  
  
Wheel
                            slip, ie driven minus ground  
  
Wheel
                            Diff  
  
  
  
  
  
Speed
                            difference between two ground speeds  
  
Wideband
                            Sensor 1  
  
Lambda 1  
  
AFR Left  
  
Haltech
                            sends as lambda, so do we, on the dash default
                            configuration it’s displayed as lambda and shows “L”
                            as the unit. If you want it in AFR there’s probably
                            a dash configuration option you can change or an
                            input scaling.  
  
Wideband
                            Sensor 2  
  
Lambda 2  
  
AFR Right  
  
  
  
Battery
                            Voltage  
  
Voltage_12V  
  
  
  
  
  
Coolant
                            Temperature  
  
ECT  
  
  
  
  
  
Air
                            Temperature  
  
MAT  
  
  
  
  
  
Fuel
                            Temperature  
  
Fuel T  
  
  
  
  
  
Oil
                            Temperature  
  
Oil P  
  
  
  
  
  
Target
                            Lambda  
  
Target
                            Lambda  
  
Lambda
                            Target  
  
This was
                            not implemented in the standard Haltech AEMCAN file.
                            To implement it, see belo  
  
Adding Target Lambda:  

- Go the display settings, CAN Receive
- Find the AFRTarget_Raw row.
- If the Ext shows a green tick, double click the
                      Ext checkbox to force it to the standard 11 bit CAN ID
- Change the CAN ID to 0x3e9
- Start bit = 40, length = 16, unsigned integer,
                      BE/ Motorola  
![7_AEM_6_Target_Lambda](../images/051_AEM_Dash/7_AEM_6_Target_Lambda.png)  
  
Next go to the Scalars tab, find AFRTarget_scalar
                  and set it to 0.001 with an offset of zero. The Haltech lambda
                  is divided by 1000, so a value of 1000 means stoichiometry.  
  
![8_AEM_7_Target_Lambda_Scalar](../images/051_AEM_Dash/8_AEM_7_Target_Lambda_Scalar.png)  
  
Using the[
                    Adaptronic Native Protocol](file:///C:/Users/Larry%20Cruz/Dropbox/2018/Scratch/Using%20Blue%20Griffon%20to%20edit%20Eugene%20HTML%20help%20files/EN/EN_MOD_050_ADAPCAN.md):  
  
The second method, which is a little bit more work
                  to set up but gives much better control, is to use the
                  Adaptronic native protocol. Rather than try to map all of the
                  Adaptronic variables to the AEM variables, these are just
                  given the same names as in the Adaptronic software.  
  
The way to import them all is to do as follows.
                  First we must clear the existing channels, which will probably
                  be set up for the AEM ECU:  

- Go to Setup -> Display
- Select the Outputs tab
- Select the first output name, and click
                      “Delete” at the bottom right, to remove this channel.
- Now that the “Delete” button has the focus, you
                      can hold down the enter key and it will delete all the
                      channels
- Go to the CAN Receive tab
- Again click the top row, and click Delete
- Hold down Enter to delete all the CAN receive
                      channels
- Go to the Scalars tab
- Again click the top row, and click Delete
- Hold down Enter to delete all the CAN receive
                      channels
- Go back to the CAN Receive tab
- Click “Import CAN…”
- Select the appropriate DBC file  
The standard DBC files are available in this
                  article. If you have enabled specific other channels to be
                  output, you can also generate the DBC file from the software.  
  
In the standard DBC filenames, the following terms
                  have the following meanings:  

- Standard – means that it includes all the
                      channels which are always output from the ECU
- Full – means that it includes all 1024
                      channels. Some names will be blank and therefore you will
                      get conflict errors when they are imported  
The unit scaling is done in the CAN importation
                  because the dash is not unit-aware. The following suffices are
                  used for different unit combinations:  
Filename
                            suffixAFR / Lambda
                            unitPressure unitTemp and SpeedImperial_AFRPetrol
                          AFRPSIFahrenheit
                          / mphImperial_LambdaLambdaPSIFahrenheit
                          / mphMetric_AFRPetrol
                          AFRkPaCelcius
                          / km/hMetric_AFR_PSIPetrol
                          AFRPSICelcius
                          / km/hMetric_LambdaLambdakPaCelcius
                          / km/h  
If you have selected some additional CAN channels to
                  be output in the software, then you can generate a DBC file
                  from the software. When doing this, you must select the output
                  units for scaling for AFR/Lambda, mph / km/h, PSI / kPa and
                  Celcius / Fahrenheit.  
  
DBC Files:  
  
[Adaptronic
                    Full Imperial AFR](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Full_Imperial_AFR.dbc)  
[Adaptronic
                    Full Imperial Lambda](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Full_Imperial_Lambda.dbc)  
[Adaptronic
                    Full Metric AFR](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Full_Metric_AFR.dbc)  
[Adaptronic
                    Full Metric AFR PSI](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Full_Metric_AFR_PSI.dbc)  
[Adaptronic
                    Full Metric Lambda](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Full_Metric_Lambda.dbc)  
[Adaptronic
                    Standard Imperial AFR](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Standard_Imperial_AFR.dbc)  
[Adaptronic
                    Standard Imperial Lambda](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Standard_Imperial_Lambda.dbc)  
[Adaptronic
                    Standard Metric AFR](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Standard_Metric_AFR.dbc)  
[Adaptronic
                    Standard Metric AFR PSI](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Standard_Metric_AFR_PSI.dbc)  
[Adaptronic
                    Standard Metric Lambda](http://www.adaptronic.com.au/files/DBC%20Files/Adaptronic_Standard_Metric_Lambda.dbc)  
  
Big thank you to @Aaparkah.300 – Aaron Parker for
                  lending us the dash for testing.  
  
©2018
        Adaptronic  
