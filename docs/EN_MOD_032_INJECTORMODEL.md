How Fuel Mass is Converted to Milliseconds on Modular ECUs/*

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
  


How Fuel Mass is Converted to Milliseconds on
              Modular ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Injection
                Timing on Port Injected Engines](EN_MOD_035_INJECTORTIMING.md)[
              ](EN_EUGENE_ABOUT.md)

[Selecting
                Injectors](EN_MOD_040_INJECTOR_SELECTIONINSW.md)

  


[  

              ](EN_SelFW.md)

  


  
  
[](https://youtu.be/TDNA3OeWp-4)  
  
  
If you’ve see the other videos or articles about how the ECU
                  calculates the amount of fuel to be delivered, you’ll have
                  seen that the end result of those is in the units of fuel
                  mass, not milliseconds. This article explains how the ECU
                  converts from fuel mass into milliseconds, and a bit about how
                  injectors behave.  
  
Firstly, let’s talk about injectors. A fuel injector for low
                  pressure EFI, as used on every port injected engine, is an
                  electromechanical device. It has mechanical and electrical
                  properties which are often not that well understood.  
  
![1_injector](../images/032_InjectorModel/1_injector.png)  
  
In this description I’m going to talk about fuel pressure.
                  When I talk about fuel pressure, I’m talking about the
                  differential fuel pressure across the injector, ie the fuel
                  gauge pressure minus the manifold gauge pressure. If you have
                  a manifold referenced regulator, this should be pretty much
                  constant.  
  
![2_Fuelpressure](../images/032_InjectorModel/2_Fuelpressure.PNG)  
  
![3_MR](../images/032_InjectorModel/3_MR.png)  
  
Manifold Referenced Regulator  
  
The fuel injector is designed so that the fuel pressure holds
                  the injector closed. The injector contains an electromagnet,
                  or solenoid, which pulls the injector open against this fuel
                  pressure force. The force which the solenoid exerts is
                  proportional to the current flowing through it, and therefore
                  you need a certain current to overcome the fuel pressure and
                  cause the injector to open.  
  
Electrically, the solenoid has inductance and resistance. So
                  its response can be written using the differential equation:  
  
v = L di/dt + iR  
  
where:  

- L is the inductance
- R is the resistance
- i is the instantaneous current
- v is the instantaneous voltage  
If you’re not familiar with differential equations, you might
                  be able to see or guess that the injector current depends on
                  the voltage that’s applied to it. A higher voltage gives you a
                  higher injector current. Not only that but the higher voltage
                  also causes the current in the injector to build up faster.
                  Therefore the amount of time it takes for the injector to open
                  depends on the voltage applied to it.  
  
Furthermore, at higher fuel pressures, higher injector current
                  is required for the injector to open. Therefore the amount of
                  time it takes for the injector to open depends on both fuel
                  pressure and supply voltage.  
  
Below is an example response from an aftermarket injector, the
                  Siemens 220lb/hr, taken at 3 bar of fuel pressure.  
  
This graph should be a straight line, intercepting the X-axis
                  at the amount of time it takes for the injector to open, and
                  then going up from there at a slope determined by the injector
                  flow rate.  
  
  
![4_xint](../images/032_InjectorModel/4_xint.png)  
  
X-intercept is the line pointed by the arrow  
  
In practice we see several lines. These correspond to
                  different supply voltages for the injector. You can see that
                  the higher voltages cause the injector to open more quickly,
                  but once the injector is open, the fuel flow rate is basically
                  independent of voltage.  
  
If you have sharp eyes you will also see that at low opening
                  times, that is if we’re trying to deliver 25µL of fuel or
                  less, the curve has a bit of a kink to it. This is because of
                  pintle bounce – you only see this on underdamped injectors;
                  many don’t exhibit this behaviour at all. But what it means is
                  that if you want to deliver less than 25µL of fuel, it’s going
                  to be hard to achieve that accurately with this particular
                  injector.  
  
![5_computation](../images/032_InjectorModel/5_computation.png)  
  
For every injector at any given pressure, there is a minimum
                  voltage required to open. We find in testing some injectors
                  that many of them won’t open at say 5 bar fuel pressure at a
                  low voltage like 7 or 8 Volts. In some cases injectors don’t
                  open reliably with 4 bar at 9V. You might be asking the
                  question “who cares; I have a decent charging system on my
                  car” but your charging system isn’t working when you’re
                  cranking the engine. It’s very common to see the supply
                  voltage drop to 8 or 9 volts during cranking, and if you’ve
                  upgraded your injectors to larger ones, but they aren’t high
                  powered enough to open at the low voltage at your nominate
                  fuel pressure, you’re going to be wondering why your engine
                  won’t start. People sometimes misdiagnose this – because after
                  you let go of the starter the voltage recovers quickly as the
                  engine is still spinning down, so the ECU is still injecting
                  fuel pulses during this time. Then when they hit the key the
                  second time, it starts. Because they haven’t diagnosed the
                  problem correctly they say that their problem is it always
                  takes 2 attempts to start, rather than my injectors aren’t
                  opening during cranking. Both are correct but the first one
                  would have you chasing cranking fuel settings when that’s not
                  the problem.  
  
Fuel injectors are essentially volume delivery devices,
                  because their flow rate does not change very much with
                  temperature. Therefore in this translation from mass to
                  milliseconds, we need to first calculate the volume.  
  
The ECU calculates the density of the fuel based on the
                  stoichiometric ratio, and the temperature if enabled. The
                  stoich ratio can be a constant, or it can be measured from a
                  flex sensor, but either way the ECU calculates the basic
                  density from this.  
  
If under the fuel system settings you enable “trim for fuel
                  density”, then the ECU will also compensate for changes to the
                  fuel density due to temperature (which themselves differ
                  between E0 and E100). This requires a fuel temperature sensor,
                  which can either be wired in, or you can read the fuel
                  temperature from a flex fuel / ethanol sensor.  
  
![6_trimfuel](../images/032_InjectorModel/6_trimfuel.png)  
  
The current estimate of the fuel density is one of the
                  variables that you can see in the gauge window under
                  Intermediate Calculated Variables.  
  
![7_fueldensity](../images/032_InjectorModel/7_fueldensity.png)  
  
From the mass and the density, the ECU now knows the fuel
                  volume to deliver. This volume is split between the different
                  stages in accordance with the algorithm I described in the
                  injector staging video. Then each volume for each injector is
                  converted into a millisecond duration. This is done as
                  follows.  
  
Firstly, you can specify a minimum fuel volume for the
                  injector to deliver. If you enter a non-zero value in this
                  setting, the ECU will “clip” the value using this as a
                  minimum. For example if you look at the injector performance
                  graph and find that the injector is unreliable at less than 10
                  µL, you can enter 10µL and instead of the ECU trying to
                  deliver 8 which might result in missing fuel all together, it
                  will deliver 10.  
  
![8_minfuel](../images/032_InjectorModel/8_minfuel.png)  
  
Secondly, the ECU then calculates the effective on-time from
                  knowing the flow rate and the volume required to be delivered.  
  
For those who prefer to think in effective milliseconds rather
                  than fuel volume, the Modular ECUs also have a minimum
                  effective on-time which can clip the fuel duration, so you can
                  use either this one or the volume based one. Just set the
                  other one to zero so they both aren’t working together!  
  
![9_mineffective](../images/032_InjectorModel/9_mineffective.png)  
  
Next, the ECU has a 3D map of offset, or dead-time, as a
                  function of battery voltage and fuel pressure. Note that this
                  is the differential fuel pressure, so the pressure across the
                  injector. This can be determined in 2 ways.  
  
![10_dedtime_1](../images/032_InjectorModel/10_dedtime_1.png)![11_dedtime](../images/032_InjectorModel/11_dedtime.png)  
  
The first way is to measure it directly using a fuel pressure
                  sensor. See the sensor setup video for information on how to
                  configure pressure sensors. The ECU then measures the fuel
                  pressure and subtracts the manifold pressure to determine the
                  differential fuel pressure, which is a variable you can see on
                  the gauges window and should be fairly much constant with a
                  manifold-referenced regulator. The ECU then uses this value to
                  look up the offset and flow rate the injector settings.  
  
The second way is to use a nominal figure that you enter. For
                  this, there are two types of fuel systems that we support; one
                  is the manifold-referenced pressure regulator, where the
                  pressure regulator aims to achieve a constant differential
                  fuel pressure. The other is the fixed pressure, where this is
                  no hose from the inlet manifold to the pressure regulator, and
                  the gauge fuel pressure is constant. In this mode, the
                  differential fuel pressure varies based on manifold pressure,
                  so the ECU needs to know this to know to look up different
                  flow rates and offsets as the differential fuel pressure
                  changes.  
  
  
![12_FR](../images/032_InjectorModel/12_FR.png)  
  
Fixed Fuel Regulator  
  
You can enter these tables manually if you have the equipment
                  and expertise to characterise injectors, or you can select
                  from a set of predefined injectors that we have already
                  characterised. I need to give a big thank you to Paul Yaw from
                  Injector Dynamics for his assistance with the
                  characterisation.  
  
If you select a predefined injector for which we have the
                  short pulse correction information, which is all of the
                  Injector Dynamics injectors, this is added automatically by
                  the firmware.  
  
Note that the current offset and flow rates are also displayed
                  in the gauges under intermediate calculated values so that you
                  can see what the ECU believes the injector to be doing.  
  
One last point; watching the differential fuel pressure is
                  very instructive. If you have a decent pressure regulator like
                  a Turbosmart FPR800 or 2000, the differential fuel pressure
                  hardly moves at all; it’s very stable. If you see it move more
                  than about 10 kPa then there’s some kind of a problem. We’ve
                  been able to diagnose poor fuel pressure regulators on
                  customers’ cars very quickly by watching this variable alone,
                  and we highly recommend adding a fuel pressure sensor to any
                  car that you’re tuning, for the simple reason that fuel
                  pressure makes such a big difference, and as someone said… I
                  can’t remember who, probably an American like Shane
                  Tecklenberg, Greg Banish or Paul Yaw, if you don’t have data,
                  you have an opinion!  
  
![13_turbosmart](../images/032_InjectorModel/13_turbosmart.PNG)  
Thank you.  
©2018
        Adaptronic  
