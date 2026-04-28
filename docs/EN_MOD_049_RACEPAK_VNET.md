Using a Racepak IQ3 dash with a Modular ECU/*

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
  


Using a Racepak IQ3 Dash with a Modular ECU

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[CAN
                Protocol and the Adaptronic CAN System](EN_MOD_050_NATIVECAN.md)[
              ](EN_EUGENE_ABOUT.md)

[Setting
                up the AEM CD7 Dash  

              ](EN_MOD_051_AEMDASH.md)

  


[  

              ](EN_SelFW.md)

  


  
  
  
  
  
  
About the Racepak system:  
  
Racepak has its own implementation of CAN which it calls
                    VNET. This is a 250 kbps bus, where different CAN IDs are
                    allocated for different variables which can be transmitted
                    and logged.  
  
As well as the CAN IDs being broadcast to transmit data,
                    there is a separate protocol which allows information about
                    the data to be read and written (you can consider this the
                    “settings”). Any scaling / offsetting is done in
                    the sensor interface (or EFI interface) itself, and the dash
                    only displays or logs these scaled data. Therefore to change
                    units between metric and imperial, this must be done not in
                    the dash setting, but in the device generating the data (in
                    this case, the ECU).  
  
The pinout on the VNET connector is as follows:  
  
  
![1_Racepak_pinout](../images/049_Racepak_VNET/1_Racepak_pinout.jpg)  
  
The
                    wire colours of the VNET cable which we used to wire up are
                    as follows:  
  
PinColourFunctionConnectionGreenPower
                          groundNo
                          connection required if the dash has its own
                          power. Otherwise you can connect this to
                          power ground at the ECU to provide power to the dashRed12V
                          supplyNo
                          connection required if the dash has its own
                          power. Otherwise you can connect this to
                          ignition switched power at the ECU to provide power to
                          the dashBlackCAN
                          lowCAN
                          L – J2-23 on M2000 / M6000WhiteCAN
                          highCAN
                          H – J2-15 on M2000 / M6000DrainShield
                          wireNo
                          connection  
The
                    two other pins are unused on the VNET connection, but on the
                    Haltech branded IQ3 are the CAN connections to the
                    Haltech ECU.  
  
![2_Haltech_pinout](../images/049_Racepak_VNET/2_Haltech_pinout.jpg)  
  
ECU
                    settings:  
  
The following ECU settings must be
                  set up to use the Racepak mode directly:  

- CAN bitrate =
                      250 kbps
- CAN
                      termination = ON, if this is the last or only device on
                      the chain. Otherwise if it’s in the middle of
                      the chain then CAN termination = OFF
- CAN
                      output mode = Racepak
- Unit
                      selections according to your personal preference.  
[![3_ECUSettings](../images/049_Racepak_VNET/3_ECUSettings.jpg)](http://www.adaptronic.com.au/wp/wp-content/uploads/2017/08/ECUSettings.jpg)  
The
                    following unit selections are available:  
  
  
Setting name  
  
Options  
  
Scaling  
  
Temperature  
  
Celcius  
Fahrenheit  
  
Native = Celcius
                            (0.1 degree resolution)  
Fahrenheit = C * 9/5 + 32  
  
Speed  
  
km/h  
mph  
  
Native = km/h
                            (0.1 km/h resolution)  
mph = km/h / 1.6  
  
Lambda  
  
Lambda  
Petrol AFR  
  
Native = lambda
                            (0.001 resolution)  
Petrol AFR = lambda * 14.7  
  
Fuel / oil
                            pressure  
  
kPa  
PSI  
  
Native = kPa
                            (0.1 kPa resolution)  
PSI = kPa *0.145  
  
MAP  
  
kPa  
MGP, kPa  
MGP, PSIg  
MGP, PSIg / inHg  
  
Native = kPa
                            absolute (0.1 kPa resolution)  
MGP = MAP – baro (still in kPa)  
MGP PSIg = MGP * 0.145  
MGP PSIg  = MGP * 0.145, MGP >=0  
MGP * 0.290, MGP <= 0  
  
Dash settings:  
  
Start with the IQ3 configuration file supplied by
                    Adaptronic. This has the channels for the ECU data already
                    loaded, so that they can be selected on the dash
                    screen.  
  
[IQ3_Config_Modular.rcg](http://www.adaptronic.com.au//files/IQ3_Config/IQ3_Config_Modular.rcg)  
[IQ3_Config_Modular_Remap_forHaltechIQ3V2.rcg](http://www.adaptronic.com.au//files/IQ3_Config/IQ3_Config_Modular_Remap_forHaltechIQ3V2.rcg)  
If
                    you attempt to read out the full VNET settings, you will be
                    presented with this warning:  
  
![4_errorToIgnore](../images/049_Racepak_VNET/4_errorToIgnore.PNG)  
  
You should click “no to all” to
                  avoid the channels being deleted.  
  
Note also that the Datalink
                  software will allow you to see settings in these channels (eg
                  scaling), but changing them will have no effect. To change the
                  scaling for different units, please use the Adaptronic
                  software Eugene.  
  
The following are the data
                  generated by the Adaptronic ECU in Racepak output mode, as of
                  firmware 0.140:  
  
  
CAN address
                              (hex)  
(remap address in brackets)  
  
Variable name  
  
Decimal
                              places  
  
Units  
  
750 (768)  
  
RPM (engine
                            speed)  
  
0  
  
RPM  
  
751 (769)  
  
ECT (coolant
                            temp)  
  
1  
  
°C, °F  
  
752 (76a)  
  
Oil Pressure  
  
1  
  
kPaG, PSIg  
  
757 (76f)  
  
Ignition advance
                            (leading)  
  
1  
  
° BTDC  
  
755 (76d)  
  
IMAP (intake
                            manifold absolute pressure)  
  
1  
  
kPaA, kPaG, PSIg, PSIg /
                            -inHg  
  
753 (76b)  
  
Pedal / TPS  
  
2  
  
%  
  
75A (772)  
  
Lambda  
  
2  
  
Lambda, petrol
                            AFR  
  
75F (777)  
  
Vehicle speed  
  
1  
  
km/h, mph  
  
756 (76e)  
  
Fuel pressure
                            (gauge)  
  
1  
  
kPaG, PSIg  
  
758 (770)  
  
Injector 1 duty  
  
2  
  
%  
  
754 (76c)  
  
MAT (air
                            temperature)  
  
1  
  
°C, °F  
  
765 (77d)  
  
EGT1  
  
1  
  
°C, °F  
  
760 (778)  
  
Transmission
                            Gear  
  
2  
  
(I don’t know
                            why gear has 2 decimal places by default in the
                            Racepak system)  
  
761 (779)  
  
Battery voltage  
  
2  
  
V  
  
766 (77e)  
  
Oil temperature  
  
1  
  
°C, °F  
  
  
The default function is to have
                  the remap disabled, and the base address = 750. The remap is
                  for compatible which will be explained later for the Haltech
                  IQ3 dash.  
Haltech cobranded IQ3  
  
There are at least three versions
                  of the Haltech IQ3.  
  
Early
                    version:  
  
The first version read the Haltech
                  V1 protocol. This was actually based on the AIM protocol. The
                  Modular ECU can output this protocol by selecting:  

- The
                      output mode as Haltech V1
- The
                      bit rate as 1 Mbps
- Terminate
                      = ON  
![5_Haltechsettings](../images/049_Racepak_VNET/5_Haltechsettings.jpg)  
  
The CAN output from the ECU must
                  be connected to the Haltech CAN pins on the red
                  connector, shown above. These pins are different from the VNET
                  CAN connection.  
This works, however:  

- The
                      Oil Temperature channel was never implemented on the
                      Haltech V1 ECU, so the ECU always sent zero on this
                      channel. I believe it was never programmed correctly in
                      the Racepak EFI module, because when we output
                      the oil temperature to this channel, it is not displayed
                      correctly on the dash.
- The
                      same problem occurs with the EGT channel.
- MAP
                      is output as gauge pressure (MGP); fuel and oil are also
                      output as gauge pressure.To change units, you will need to
                      change the scaling by using the Racepak Datalink software.  
  
You can also user the
                      method for the later version, described below.  
  
Later
                        version:  
  
Haltech stopped supporting the V1
                      protocol on the Haltech IQ3 dash, and started to
                      support the Haltech V2 protocol instead, but with
                      additional authentication to ensure that the ECU connected
                      is a Haltech ECU. So even outputting the Haltech V2
                      protocol option, this does not work with the Haltech IQ3
                      V2 dash.  
  
The Haltech IQ3 dash supports VNET
                      also, so you can use the VNET
                      connection. However the data from the ECU then
                      conflicts with the data from the inbuilt Haltech protocol
                      converter. To counteract this, the Modular ECU allows you
                      to remap the CAN IDs, by adding 18 (hex) to the address.
                      For example, RPM becomes 768 instead of 750. These
                      remapped addresses are described in the
                      table above, and are already programmed in the
                      file IQ3_Config_Modular_Remap_forHaltechIQ3V2.RCG.  
  
For this connection you need to
                      connect the Adaptronic CAN pins to the VNET
                      pins, not the Haltech connection pins. On the red
                      connector cable, these two pins are not connected, so you
                      may need to buy a Racepak cable to be able to connect to
                      these pins.  
  
IQ3 Street:  
  
The IQ3 street works using the connection described in the
                    “early version” above (ie connecting the same way as a
                    Haltech ECU), and selecting the Haltech V2
                    protocol. Although we haven’t  
  
![6_Remap](../images/049_Racepak_VNET/6_Remap.jpg)  
  
©2018
        Adaptronic  
