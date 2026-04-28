Twin Turbo Control on Modular ECU/*

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
  


Twin Turbo Control on Modular ECU

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Target
                Boost Modes  

              ](EN_MOD_043_TARGETBOOST.md)

[Turbo
                Speed Sensors  

              ](EN_MOD_045_TURBOSPEED.md)

  


[  

              ](EN_SelFW.md)

  


  
  
  
  
  
In the early to late 1990s, it was common for some halo cars
                  to run twin turbocharger systems. We saw this with the Nissan
                  GTR from the R32 to the R34, the Mazda RX7 FD and the Supra
                  JZA80. Broadly speaking, there are two types of twin turbo
                  systems; the parallel systems as on the RB26 Nissan engines,
                  and the sequential twin turbos as on on the RX7 and the Supra.
                  This article will only discuss the sequential twin turbo
                  system on the RX7 FD.  
  
  
![Turbo_dSupercharged_Skyline](../images/016_TwinTurbo/Turbo_dSupercharged_Skyline.jpg)  
  
Parallel twin turbo systems  
  
![mazda-rx7-fd-13b-twinscroll-turbo-manifold-content-16](../images/016_TwinTurbo/mazda-rx7-fd-13b-twinscroll-turbo-manifold-content-16.jpg)  
  
Sequential twin turbo systems  
  
The two turbochargers are both the same size on the standard
                  RX7, however at low RPM, only one turbo is active. At high
                  RPM, or the full-power condition, both turbochargers are
                  active. This allows rapid spooling of the small turbo at low
                  RPM, while not being limited by its restriction at high RPM,
                  because at high RPM you have two of them working and therefore
                  double the flow capacity.  
  
![TTDiagramLow](../images/016_TwinTurbo/TTDiagramLow.png)  
  
![TTDiagramHigh](../images/016_TwinTurbo/TTDiagramHigh.png)  
  
When only the primary turbo is running, all the engine exhaust
                  goes through either the primary turbine, or bypasses the
                  turbine through the wastegate. The compressed air from the
                  primary turbo is fed into the intercooler after which it goes
                  up to the throttle and intake manifold. Note that in this
                  case, the compressor exit from the secondary turbo has to be
                  blocked off, otherwise the compressed air from the primary
                  turbo would feed back through it, which would mean it wouldn’t
                  produce any boost.  
  
![TurbochargerBig_final_image](../images/016_TwinTurbo/TurbochargerBig_final_image.jpg)  
  
So in this condition, the inlet charge control flap is closed,
                  and the turbo control valve is also closed, to prevent exhaust
                  going through the secondary turbine.  
  
At high RPM, we must open both of these flaps, to allow the
                  second turbo to share in the exhaust from the engine, and to
                  contribute compressed air into the inlet. So in this
                  condition, both flaps are open.  
  
In the RX7 system, there are two chambers which check valves
                  going to the inlet manifold. One is pressurised with boost
                  air, and the other stores vacuum. The solenoids that control
                  these flaps are configured so that each flap actually has two
                  solenoids, that each connect either boost or vacuum to one
                  side of a servo diaphragm. Therefore in one position, one side
                  of the diaphragm has boost and the other has vacuum, and in
                  the other position the two are swapped around. Therefore it is
                  necessary for both solenoids to be working, on all the flaps
                  which need to be controlled (both the intake and the exhaust,
                  and there is a second one in the exhaust I will describe
                  later), and the hoses all need to go to the correct locations.  
  
![chambers](../images/016_TwinTurbo/chambers.PNG)  
  
The tricky part comes with the transition. You can imagine
                  that if you’ve just been boosting hard on the first turbo, and
                  you engage the second turbo straight away by moving both the
                  exhaust and inlet flaps at once, then you’re going to get a
                  dose of turbo lag until the second turbo comes up to speed so
                  it’s producing the same boost as the primary turbo. This gets
                  worse the more boost you have on the primary turbo, for two
                  reasons. The first reason is that the first turbo loses boost,
                  because you’re diverting exhaust to the secondary turbo to
                  spool it up. The second reason is that the secondary turbo
                  actually needs to spin up to a higher speed to match the boost
                  of the primary turbo.  
  
Mazda weren’t silly so they added in what they call a
                  “precontrol valve”. This allows a small amount of air to be
                  diverted through the secondary turbine. It does cause a drop
                  in boost of the primary turbo but it’s not too extreme.
                  Secondly, there is a blow-off valve (charge relief valve) on
                  the outlet of the secondary turbo, which is under ECU control.
                  As you’d know it’s possible to overspeed a turbo by not
                  “loading” it, ie letting it just breathe into the atmosphere
                  and not deliver any boost. So what is done is for a very short
                  amount of time, we can open this precontrol valve, and the
                  charge relief valve at the same time, to get the secondary
                  turbo to spin up. Once it’s spun up, we can switch over the
                  intake flap and main exhaust flap to allow both turbos to do
                  the job.  
  
  
![dyno_twin2](../images/016_TwinTurbo/dyno_twin2.JPG)  
  
Dyno graph with PWM precontrol valve  
![dyno_twin3_PWMvsOnOff](../images/016_TwinTurbo/dyno_twin3_PWMvsOnOff.JPG)  
Sample dynograph  
  
  
How long we need to spin up the second turbo for depends
                  really on the turbo inertia, and that determines the time. So
                  doing this over an RPM window won’t be very useful because
                  that RPM window will correspond to a different time in
                  different gears, boosts and so on. So instead we actually tell
                  the ECU the time for which we want to spin up the second
                  turbo, and the RPM we want to finish by. The ECU looks at the
                  current rate of change of RPM and the current RPM to work out
                  when it needs to start the precontrol period. Previously we
                  have used a short period and just turned on the precontrol
                  output hard, but it turns out that starting earlier and pulse
                  width modulating the precontrol output period tends to keep
                  the boost up and smooths out the power curve.  
  
In terms of the settings, the ECU needs a minimum MAP and a
                  minimum TPS to activate the twin turbo function. Then there is
                  the RPM to enable the secondary turbo, and the pre-control
                  duration as described just before.  
  
The values we have used are 4400 RPM and 1200 ms (or 1.2
                  seconds).  
  
![TTsettings](../images/016_TwinTurbo/TTsettings.PNG)  
  
This feature is a bit redundant now since turbo technology has
                  come such a long way, and there are many single turbochargers
                  that behave as well as the factory twins, but many series 8s
                  are still running the factory twins so this function is
                  needed.  
  
Lastly, we need to talk about the outputs. The easiest way to
                  do this is with a plug and play ECU. But if you’re wiring in,
                  then please observe the following:  
1) The charge control valve and the turbo control valve need
                  to be opposite polarity. Therefore enable one in the software
                  as Twin Turbo, ann the other as Twin Turbo, inverted  
2) The precontrol output needs to be inverted, and as I said
                  above, making it PWM even at say 25 Hz does help with the
                  power curve.  
3) The charge relief valve can be connected in parallel with
                  the twin turbo output control  
Thank you!  
©2018
        Adaptronic  
