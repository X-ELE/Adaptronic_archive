CAN Protocol and the Adaptronic CAN System/*

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
  


CAN Protocol and the Adaptronic CAN System

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Using
                a Racepack IQ3 Dash](EN_MOD_049_RACEPAK_VNET.md)[ ](EN_EUGENE_ABOUT.md)

[Setting
                up the AEM CD7 Dash  

              ](EN_MOD_051_AEMDASH.md)

  


[  

              ](EN_SelFW.md)

  


  
  
  
  
  
This article describes the CAN
                  protocol in general, and also describes the native Adaptronic
                  CAN system.  
  
Firstly, CAN is short for Control Area Network. It
                  is a multi-drop broadcast protocol. The physical connection is
                  via a twisted pair; with a high and a low signal. When the bus
                  is in the recessive state, both high and low signals are at
                  the same voltage. When the bus is in the dominant state, the
                  high line goes to a higher voltage and the low line goes to a
                  lower voltage, with the average voltage remaining the same.
                  This provides excellent noise immunity and is a similar
                  principle to many other protocols such as RS485, RS422,
                  Ethernet and even good old analog phone lines – none of which
                  are shielded usually.  
![1_resistor](../images/050_NativeCAN/1_resistor.jpg)CAN
                        Bus Diagram  
![2_Recessive](../images/050_NativeCAN/2_Recessive.png)![3_Dominant](../images/050_NativeCAN/3_Dominant.png)  
  
Multiple devices can be connected on the
                  bus in parallel, and there is no bus master; any device can
                  broadcast a message. The bus should be terminated at each end
                  with a 120 Ohm resistor.  
  
Because of the way CAN works, every device on the
                  bus must be set to the same bit rate. If you have two devices
                  with different bit rates on the bus, then as soon as one
                  starts to broadcast a message, the second one will see that
                  the message is corrupt (because the bitrate is wrong) and
                  actually transmit over the top to ensure that no other devices
                  can misbehave due to the corrupt message. Therefore it is very
                  important to make sure you understand the bitrates of the
                  different devices on the CAN bus.  
  
Each CAN data packet contains an identifier, which
                  is either 11 or 23 bits in length, and then up to 8 data
                  bytes. The identifier is what allows the other devices on the
                  bus to know which device sent the message and what it means.  
  
All Modular ECUs have at least one CAN bus, with
                  many such as the M6000 having a second CAN bus connection. All
                  the settings and functions are the same for both busses, so we
                  will only discuss one of them here.  
  
  
[
                  ](http://www.adaptronic.com.au/wp/wp-content/uploads/2017/08/2_terminator.jpg)![4_2CAN](../images/050_NativeCAN/4_2CAN.png)  
  
In the Adaptronic software there are many CAN
                  settings, and I won’t discuss them all in this article, but we
                  will discuss the basics. The first is the bitrate, as
                  discussed earlier. The default is 1 Mbps, which is also the
                  highest rate, however lower rates can also be selected so long
                  as they divide into 1 Mbps. You can also select an option here
                  to disable the CAN function completely, and that allows the
                  bus to be free (without bitrate conflicts described before).  
  
![5_Bitrate](../images/050_NativeCAN/5_Bitrate.jpg)  
  
The second is the inbuilt termination resistor; the
                  ECU has an internal 120 Ohm resistor to terminate the CAN bus,
                  and that can be enabled or disabled using the software
                  setting. In accordance with what I described before about a
                  CAN bus needing a 120 Ohm resistor at each end of the bus,
                  this means that you should enable the termination resistor if
                  the ECU is located at one END of the CAN bus, but if it’s in
                  the middle, this should be disabled and the termination should
                  be done at each end.  
  
![6_terminator](../images/050_NativeCAN/6_terminator.jpg)  
  
There are settings for receiving wideband over CAN,
                  and also the non-native CAN output modes such as emulation of
                  the[Racepak](file:///C:/Users/Larry%20Cruz/Dropbox/2018/Scratch/Using%20Blue%20Griffon%20to%20edit%20Eugene%20HTML%20help%20files/EN/EN_MOD_049_RACEPAK.md)or Haltech systems, but I won’t go into those here.  
  
![7_Wideband](../images/050_NativeCAN/7_Wideband.jpg)  
  
Each CAN bus can also send out data in the
                  Adaptronic native format. This gives you a direct window into
                  the live variables inside the ECU, in the same way that
                  you can see almost any variable from within the Eugene
                  software on the gauges or monitor panels.  
  
![8_CANchannels](../images/050_NativeCAN/8_CANchannels.jpg)  
  
All these live variables are 16 bits – so each
                  variable takes 2 bytes. Therefore, 4 of these can fit into a
                  CAN packet. The software supports up to 1024 live variables,
                  and therefore there are up to 256 different CAN packets that
                  can be sent. Each different CAN packet has a unique ID. The
                  default base address is $300, so therefore these CAN packets
                  can have the IDs in the range of $300 - $3ff. You can select
                  which channels are transmitted, so that you can avoid a whole
                  lot of data you don’t need and maximise the data rate.  
  
The settings available are as follows:  

- Bitrate, described above. The default is 1 Mbps
- Termination, the default is “on”
- Enabling of the Adaptronic CAN output
- The base address, default being $300
- Enabling of any additional CAN channels  
The channels which are always transmitted include
                  the basics like engine speed, battery voltage, manifold
                  pressure, throttle position and so on. They will appear at the
                  bottom.  
  
In addition you can send any of the
                  variables, which you can select in the software.  
  
Furthermore, you can select a function in the
                  software which generates a document showing all the variables
                  which will be transmitted.  
  
The document for the standard configuration is
                  attached.  
  
©2018
        Adaptronic  
