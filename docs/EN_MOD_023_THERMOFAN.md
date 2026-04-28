Thermofan Control on the Modular ECUs/*

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
  


Thermofan Control on the Modular ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Air
                Conditioner Setup](EN_MOD_018_ACSETUP.md)[ ](EN_MOD_018_ACSETUP.md)

[Wiring
                and Configuring Outputs on Different Types of Idle Actuators  

              ](EN_MOD_024_IDLEOPSWIRING.md)

  


[  

              ](EN_SelFW.md)

  


  
  
  
  
  
In this article we’ll discuss the
                  thermofan control on the Modular ECUs.  
  
You might be already thinking, why do we need a
                  special control mode for the thermofan, can’t we just trigger
                  an output based on coolant temperature? Yes you can, but to
                  control a thermofan nicely, there’s a bit more to it than
                  that. That’s the way that we used to do it on the Select ECUs,
                  but it causes some complications, namely:  
  

- You also want the thermofans to come on when
                      the air conditioner comes on, to draw air through the
                      condenser
- You want the thermofan to come ON by default if
                      there’s no sensor connected or a sensor fault, which if
                      you use a generic output based on coolant temperature, you
                      can’t do
- You want to bump up the idle effort when the
                      thermofan switches on, especially with little engines
- Ideally, you would want to bump up the idle
                      effort slightly BEFORE turning on the thermofan, as we do
                      with the air conditioner, to avoid a dip in the idle speed
                      just after the fan or fans turn on  
With all these considerations together, we decided
                  to make the thermofan a dedicated output type on the Modular
                  ECU rather than have people implement it with a threshold
                  based on coolant temperature with a bunch of external logic to
                  make it behave really nicely.  
  
Firstly, let’s look at the different settings
                  available, and these are available in the functions ->
                  thermofan page in the software.  
  
The first is the number of thermofan stages.
                   This can be a number from 1 to 3, and represents the
                  number of different speeds or stages for the fans. For
                  example:  
  
1 fan  
  
1 stage  
  
2 fans, wired to come on at the same time (single ECU
                          output)  
  
1 stage  
  
2 fans, independently controlled (2 ECU outputs)  
  
2 stages  
  
2 fans, able to run in parallel or series or just 1
                          fan, high / low speed fans etc (3 ECU outputs)  
  
3 stages  
  
![Noofstages](../images/023_Thermofan/Noofstages.jpg)  
  
Thermofan number of stages  
  
![Stage1_2thermofans](../images/023_Thermofan/Stage1_2thermofans.png)![stage1wiring](../images/023_Thermofan/stage1wiring.jpg)![Stage2_2thermofans](../images/023_Thermofan/Stage2_2thermofans.PNG)![Stage3_thermofans](../images/023_Thermofan/Stage3_thermofans.png)  
  
A separate output pin on the ECU is required for
                  each stage that you are going to run.  
  
![Outputpins](../images/023_Thermofan/Outputpins.png)  
  
The next setting is the temperate for each stage to
                  be activated. For example if you have 2 stages, then you have
                  2 activation temperatures. When the coolant temperature goes
                  above the first stage temperature, the first stage will
                  activate. When the coolant temperature goes above the second
                  stage temperature, the second stage will activate.  
  
![2stage_turn_on](../images/023_Thermofan/2stage_turn_on.png)  
  
The next setting is the hysteresis, which is the
                  temperature drop below the activation temperature to turn off
                  the fan. As an example, if you set the temperature to 2
                  degrees and the activation temperature is 100 degrees, then
                  the coolant temperature will need to go above 100 degrees for
                  the fan to turn on, and it will turn off when the temperature
                  goes below 98.  
  
![OFFat98](../images/023_Thermofan/OFFat98.png)  
  
The next settings are the additional idle effort
                  (percentage) to be applied when each stage is active. For
                  example if you enter 3% here, the ECU will automatically add
                  3% to the idle duty cycle to help stabilise the idle speed
                  with the additional electrical load from the fan.  
  
![idleeffort_1](../images/023_Thermofan/idleeffort_1.png)  
  
![ONat100](../images/023_Thermofan/ONat100.png)  
  
The final setting is the delay. When the coolant
                  temperature exceeds the threshold, the ECU first applies the
                  additional idle effort. After the delay time, the ECU then
                  turns on the thermofan output. This helps reduce or eliminate
                  the idle dip when the fan is turned on.  
  
In addition to this logic, the fans are always run
                  at full speed if there’s a coolant temperature sensor failure,
                  or if the air conditioner is active.  
  
You can see in the software the current state of the
                  thermofan stages and the current temperature.  
  
![softwarelooks](../images/023_Thermofan/softwarelooks.png)  
  
In terms of outputs, you need to connect the relays
                  so that each stage output will drive the fans correctly. The
                  ECU will drive an output low for each stage, and lower. For
                  example if you have selected a 2 stage thermofan
                  configuration, and the ECU is trying to run the thermofans at
                  stage 2, then both outputs 1 and 2 will be on at the same
                  time.  
  
The outputs are configured in the usual way, select
                  a free output, select the category as “outputs” and select
                  “Thermofan speed 1 or greater” for the first stage output. The
                  second fan output needs to be “Thermofan speed 2 or greater”  
  
![outputsettingthermo1](../images/023_Thermofan/outputsettingthermo1.png)  
  
Once you have it all working, you should set the
                  additional idle effort as follows. Firstly, ensure that your
                  closed loop idle is working correctly. Then, watch the idle
                  effort before the fan is turned on (ie thermofan stage = 0).
                  Then when the engine heats up and the fan is turned on, watch
                  what happens to the idle effort. This new value minus the old
                  value with the fan off is what you should enter in the
                  additional idle effort for thermofan 1 setting. This can also
                  be applied to the higher stages. If the engine doesn’t get hot
                  enough to trigger the thermofan at idle, or you’re impatient
                  like me, you can artificially change the thermofan activation
                  temperature for this test.  
  
![Closedloop](../images/023_Thermofan/Closedloop.png)  
  
Once you’re happy with the extra idle effort, you
                  can adjust the delay to give the smoothest transition of the
                  fan turning on. Generally the delay should be fairly short, eg
                  200 ms. If the delay is much longer, the closed loop idle
                  control will start to correct for the extra effort when
                  there’s no corresponding load and the dip will become worse
                  and with a shorter delay. But the delay must be long enough
                  for the engine to react, or there is no benefit.  
  
There’s not a lot to troubleshoot with the thermofan
                  that isn’t obvious, but the only thing I’d suggest is that if
                  you have a problem where the fan or fans seem to be coming on
                  all the time, check that you have selected the correct number
                  of stages. If you have selected 2 stages when your car is only
                  set up for a single stage, and the second stage temperature is
                  zero, it means the ECU will see that the engine is always hot
                  (so long as the coolant temperature is above zero, because
                  that’s what you’ve set the high speed fan temperature to),
                  so  that’s more than likely the problem in this case.  
  
![Notemp_on2](../images/023_Thermofan/Notemp_on2.PNG)  
  
Wrong setup because temperature 2 is set to zero degrees  
  
![graph](../images/023_Thermofan/graph.png)  
  
Graph of themofan speed 1 output,
                  thermofan speed 2 output, thermofan speed 3 output, idle
                  effort and coolant temp. As coolant temp is ramped up
                  thermofans switched on but with time delay due to the delay
                  set in the software and as the coolant temp ramped down
                  thermofans switched off at certain temperature considering the
                  set hysteresis.  
©2018
        Adaptronic  
