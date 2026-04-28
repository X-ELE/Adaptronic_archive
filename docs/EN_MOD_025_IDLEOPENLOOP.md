Setting up Open Loop Idle Control on Modular ECUs/*

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
  


Setting up Open Loop Idle Control on Modular
              ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Setting
                up Closed Loop Idle Control](EN_MOD_026_IDLECLOSEDLOOP.md)[ ](EN_EUGENE_ABOUT.md)

[  

              ](EN_EUGENE_KBSC_TG.md)

  


[  

              ](EN_SelFW.md)

  


  
  
  
  
  
Hi all, in this video we’re going to
                  discuss how to get the basic idle settings correct. I won’t be
                  covering how to configure outputs for idle control and wire
                  them up, because that’s done in a separate video.  
  
Just like getting the fuel mixture right, getting
                  idle control right starts off with having the basic map
                  correct and then applying closed loop on top to do fine
                  tuning. So let’s look at the basic factors that go into open
                  loop idle.  
  
Firstly, let’s show where you can find the idle
                  effort in the software. You can see it on the gauges window,
                  next to RPM. The RPM field shows the current RPM, the target
                  RPM and the idle effort (which could be duty cycle, number of
                  steps or electronic throttle authority). You can also add it
                  to the monitor window and it also appears in various idle
                  setup pages.  
  
![1_idlelocation](../images/025_IdleOpenLoop/1_idlelocation.png)  
  
Now, let’s look at the cranking condition. This is
                  what happens when the engine is stopped, or when it hasn’t yet
                  reached the cranking RPM threshold, for example 300 RPM. In
                  this condition, the idle valve is held all the way open to
                  make the engine easier to start. So the idle effort will be
                  100% in this condition.  
  
Next, let’s consider what happens when the engine
                  fires. After this happens, the ECU is in the running (as
                  opposed to cranking) mode. In this mode, the ECU calculates
                  the idle effort from the following factors:  

- Base idle effort (which depends on coolant
                      temperature)
- Post-crank idle effort (which depends on
                      coolant temperature and time)
- Additional idle effort for electrical loads,
                      air conditioner, thermofan, alternator and so on
- Closed loop control  
Initially, we’ll turn closed loop idle control off.
                  This enables us to see what the actual settings are doing, as
                  opposed to how well the ECU can correct it.  
  
![2_disablecloseloop](../images/025_IdleOpenLoop/2_disablecloseloop.png)  
  
If we’re setting up the idle from scratch, we should
                  also set all the idle-up values to zero, and start off with
                  the base idle effort. This is best done with an engine
                  starting from cold. Firstly, set the target idle speed against
                  the coolant temperature; most port injected engines want to
                  run higher RPM when they are cold to combat the fuel falling
                  out of suspension at low temperatures.  
  
![3_settozero](../images/025_IdleOpenLoop/3_settozero.png)  
  
![4-1_targetidlespeedtable](../images/025_IdleOpenLoop/4-1_targetidlespeedtable.png)![4_targetidlespeedtable](../images/025_IdleOpenLoop/4_targetidlespeedtable.png)  
  
Secondly, as the engine heats up, adjust the base
                  idle effort in the base duty cycle table against coolant
                  temperature. Extrapolate past the ends as needed.  
  
![5_baseidleduty](../images/025_IdleOpenLoop/5_baseidleduty.png)![5-1_baseidleduty](../images/025_IdleOpenLoop/5-1_baseidleduty.png)  
  
The other way to do this is to enable closed loop
                  idle control, and then allow the closed loop function to
                  settle on the target idle speed. Copy the final idle effort
                  into the table at each temperature cell as it is reached.  
  
![6_enableclosedloop](../images/025_IdleOpenLoop/6_enableclosedloop.png)  
  
Next, you should set up the idle-up for loads. The
                  procedure for this is to either adjust the additional efforts
                  so that the target idle is still maintained when the load is
                  applied, or to allow the closed loop to correct the idle
                  effort, and take the difference between when the load is
                  applied and when it is not and copy that into the additional
                  idle effort. This is also described in the setup article for
                  the air conditioner and the thermofan.  
  
For idle loads which the ECU only knows about via
                  external inputs, these also need to be wired in and
                  configured. Generally these are switches which either pull to
                  ground when they are activated, for example a power steering
                  pressure switch. For this type of input, select a digital
                  input that you’re not using, connect the switch to this input,
                  and select the type as being “power steering” as an example.  
  
![7_powersteering](../images/025_IdleOpenLoop/7_powersteering.png)  
  
Another example is a headlight input. Normally this
                  goes high to 12V when the headlights are on, but is shorted to
                  ground when they are off. Again this should be connected to a
                  digital input, and then the input should be selected as an
                  electrical load, for example electrical load 1. But in this
                  case because it’s driven high when it’s active, we must select
                  “active high” in the digital input setting.  
  
![8_electricalload](../images/025_IdleOpenLoop/8_electricalload.png)  
  
When any of the electrical inputs, power steering or
                  air conditioner inputs are active, the ECU will increase the
                  target idle RPM to the “new target when on” setting in the
                  idle-up page. If this target is below the target idle speed in
                  the target idle speed table, it will use the target idle speed
                  from the table instead (ie, it uses the maximum of the target
                  idle speed from the table, and the “new target” of any
                  activated input).  
  
The “extra duty – alternator” function is for cars
                  where the ECU is able to see the alternator field current, for
                  example if the regulator is built into the ECU rather than the
                  alternator itself. This is the case with the NB and later MX5
                  / Miata, the RX8, 86/FRS/BRZ and the Dodge SRT4 and probably
                  many others. In this case you can select an input channel for
                  the field current, enter a maximum and minimum voltage for
                  that input corresponding to the min and maximum values that
                  you will see, and minimum / maximum idle efforts for these
                  conditions. Normally the minimum idle effort would be zero.
                  The ECU will scale the idle effort linearly between these two
                  and in practice it works really well; much better than with
                  digital inputs to select whether different functions on the
                  car are turned on or not.  
  
![9_Extraduty](../images/025_IdleOpenLoop/9_Extraduty.png)  
  
The final function I wanted to talk about is the
                  post-crank idle-up. This is a table with coolant temperature
                  on one axis and time on the other. Time=0 is the time where
                  the engine actually first fires, and for example 10 represents
                  10 seconds after the engine has started. This table enables
                  you to program in a post-crank flare to clear the engine out,
                  or save it from a stall or whatever is desired on that
                  particular engine. Note that it will be interpolated between
                  these points, and the maximium time you can have post-crank
                  idle for is 300 seconds or 5 minutes (in practice, if you need
                  it that long you’re probably doing something wrong). Note that
                  whenever the interpolated value from this table (ie, the extra
                  idle effort to add due to the post-crank amount) is greater
                  than 1%, the ECU will not go into closed loop idle. Obviously
                  during this post-crank flare, it’s going to be above the
                  target idle speed, and that’s where you want it, so going into
                  closed loop in this condition is not an option. So the ECU
                  will stay in open loop until the correction is down to less
                  than 1%.  
  
The only thing I’ll say about setting up the
                  post-crank idle effort is that sometimes if an engine doesn’t
                  want to rev up nicely post crank, it’s not because of the idle
                  effort but it’s instead because of poor fuelling. So if it
                  doesn’t seem happy and you want it to rev higher or clear
                  itself up, then you should check the post-crank enrichment
                  first – try 10% more or 10% less in this table first to see if
                  it makes a difference.  
  
![10_postcrank](../images/025_IdleOpenLoop/10_postcrank.png)![10-1_postcrank](../images/025_IdleOpenLoop/10-1_postcrank.png)  
  
Two final settings – one is the minimum duty cycle.
                  In most cases you can set this to zero. In some cases, setting
                  it just below the minimum that you encounter with a hot engine
                  and no electrical loads can help with idle stability. And on
                  some idle valves, below a certain duty cycle they actually
                  start admitting more air, so you need to stay away from that
                  end of the scale because non-monotonic actuators make Andy
                  cry.  
  
The final setting is “close idle on boost”. In most
                  turbocharged applications, the air for the idle control valve
                  will be taken from just before the throttle body, so it really
                  acts as an idle bypass. However in some cars, even in some OEM
                  installations like some Toyota 1JZ cars, the idle motor
                  actually gets its air source from an unpressurised source. So
                  if the idle valve remains open when the engine is on boost,
                  air leaks back through the idle valve to the air filter and
                  creates a boost leak. If you enable this setting, the idle
                  valve will be closed when the engine is on boost (by closed we
                  mean set to the minimum duty cycle).  
  
![11_final](../images/025_IdleOpenLoop/11_final.png)  
  
In a separate article, we’ll talk about closed loop
                  idle control.  
Thank you and happy learning!  
©2018
        Adaptronic  
