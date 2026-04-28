Flex Fuel Tuning on Modular ECU/*

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
  


Flex Fuel Tuning on Modular ECU

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[  

              ](EN_EUGENE_ABOUT.md)

[  

              ](EN_EUGENE_KBSC_TG.md)

  


[  

              ](EN_SelFW.md)

  


  
  
[](https://youtu.be/8-ZL3VvUoJ8)  
  
Since E85 has become commonly available, it
                  has become a popular choice of fuel for performance tuners,
                  because it’s relatively cheap and similar octane level to race
                  fuel. However it’s not available everywhere, and often people
                  with street driven cars, where it is legal to do so with an
                  aftermarket ECU, want to have the option to switch to E0 or
                  any other blend of ethanol and petrol / gasoline. Also, while
                  where I live in Sydney we have E85 at the pump, apparently in
                  the US it’s quite common for “gas stations” to advertise the
                  fuel as E85, but the ethanol content can be as low as 50%,
                  which makes it E50. So if you want to be able to run different
                  fuels without draining the tank, or use “pump E85” in the US,
                  then you need a system that can handle any ethanol percentage
                  in the fuel. This configuration is called “flex fuel” and is
                  supported by all the Modular ECUs, and all the Select ECUs
                  except the base model e420d. This article describes how to set
                  up flex fuel on the Modular ECUs.  
  
Broadly speaking there are three different variables
                  the ECU can change based on the ethanol content, which are the
                  delivered fuel quantity, the ignition timing, and the amount
                  of boost available to the driver.  
  
First let’s discuss how to install such a system on
                  the car. You will need a flex fuel sensor; also called a fuel
                  composition sensor or ethanol sensor. There are three types of
                  these; the old Siemens type, the Continental type and the Ford
                  type. We do not support the Ford type, but the Continental and
                  the Siemens have the same output configuration and we support
                  both of those.  
  
![1_flexfueltype](../images/028_FlexFuel/1_flexfueltype.png)  
  
This can either be connected in series with the
                  supply side, or the return side of the fuel going back to the
                  tank. In some cases people do things like loops to make sure
                  that the sensor stays wet even when the fuel drains away, or
                  run parallel paths so it’s not a restriction to the fuel
                  delivered to the engine, or even put the sensor in the return
                  path from a surge tank back to the main tank. There are
                  various arguments about this and if you want to start an
                  argument on the internet, go to a facebook group with a bunch
                  of tuners and tell them the right way to do it.  
  
![2_supplyside](../images/028_FlexFuel/2_supplyside.PNG)![2_returnline](../images/028_FlexFuel/2_returnline.PNG)  
  
One argument against using the return from the
                  regulator is that if you run out of fuel supply and the
                  regulator shuts off completely, then the sensor will be dry
                  and that will give an incorrect reading. The Modular ECUs
                  mitigate against this by only reading the value from the
                  sensor when the engine is in the vacuum condition; as soon as
                  the engine develops boost, the ECU “locks” the value until it
                  gets on vacuum again.  
  
One argument against using the sensor on the supply
                  side is that it’s another potential point of failure on the
                  pressurised part of the fuel system, but OEMs do this and
                  obviously they have assessed the risks. A second reason not to
                  use the sensor on the supply side is that it might cause a
                  restriction and therefore a fuel pressure drop. If you’re
                  worried about this you can always measure the fuel pressure
                  drop across the sensor; and I expect that it will be less of a
                  restriction than you think it will.  
  
The one thing I’ll say about having the sensor
                  between the surge tank and the main tank is that one of the
                  benefits of using such a sensor is that it reports not only
                  the ethanol percentage, but also the fuel temperature. The ECU
                  can use the fuel temperature to make corrections based on the
                  fuel density change with temperature, and we highly recommend
                  this, especially with E85 fuel. Some cars have fuel
                  temperature sensors fitted from the factory, for example the
                  FD RX7 and the Z32 300ZX, and ethanol’s density changes with
                  temperature more quickly that petrol’s density does. So we do
                  recommend measuring fuel temperature, and it makes sense to do
                  that with the ethanol sensor because it saves adding more
                  components and wiring. If you do want to run the flex sensor
                  at the back of the car though, and a separate fuel temperature
                  sensor, you can do that.  
  
As far as wiring goes, the flex sensor needs 12V
                  ignition switched power, ground and it has a signal output. In
                  most cases you can connect this to the CAS3 input on the ECU,
                  because most fixed valve timing and many variable valve timing
                  engines have only 2 crank or cam angle sensors. If you do need
                  to use 3 CAS inputs or more with flex fuel, then you will need
                  to upgrade the ECU with the Mini Realtime input module, which
                  gives you another 2 CAS inputs, 3 vehicle speed inputs and a
                  dedicated flex input.  
  
![3_Flexfuelsensorwiring](../images/028_FlexFuel/3_Flexfuelsensorwiring.png)  
  
Once you’ve done that, go to the ethanol input setup
                  and select the source as being “CAS3”. To measure fuel
                  temperature from the same sensor, go to Inputs ->
                  Temperature sensors -> fuel temperature. Select the type as
                  any calibration and the source as “from flex sensor”.  
  
  
[ ](http://www.adaptronic.com.au/wp/wp-content/uploads/2017/05/5_fromflex.png)![4_cas3](../images/028_FlexFuel/4_cas3.png)  
  
![5_fromflex](../images/028_FlexFuel/5_fromflex.png)  
  
The other way to get the ethanol content into the
                  ECU is to use the Innovate ECF-1 gauge. This gives ethanol
                  content, fuel temperature and lambda over one connection. To
                  configure this, firstly go to the setting for the serial port
                  you will use (serial 1 or serial 2) and select the
                  “connection” as “Innovate”. Select the type as “ECF-1”, and
                  select the number of MTXL, LC1 or LC2 as being zero.  
  
![6_innovate](../images/028_FlexFuel/6_innovate.png)  
  
![7_serial](../images/028_FlexFuel/7_serial.png)  
  
Then go to the Inputs -> Ethanol and select the
                  source as ECF over serial. The setting for the fuel
                  temperature sensor remains the same.  
  
![8_ecf](../images/028_FlexFuel/8_ecf.png)  
  
Before doing any flex tuning, you should do what we
                  always say to do and verify that the sensor is reading
                  correctly. The ethanol percentage and fuel temperature are
                  both shown in the main gauges area so you can check them
                  easily.  
  
![9_gauges](../images/028_FlexFuel/9_gauges.png)  
  
If it doesn’t display, then check the configuration
                  as I described above. If it’s connected directly through CAS3,
                  then verify that the CAS3 ARM on the F11 window flashes
                  between red and grey.  
  
![10_f11](../images/028_FlexFuel/10_f11.png)  
  
If it’s stuck at red, that means that either the
                  sensor does not have power, or that the signal wire is shorted
                  to ground. If it’s stuck at grey, that means either that the
                  sensor does not have power or that there’s an open circuit in
                  the connection between the sensor and the ECU. You can verify
                  that the wiring and the ECU are working correctly by
                  unplugging the sensor and shorting the sensor output pin on
                  the connector to ground, and verify that the ARM goes from
                  grey to red when you do that. Please remember that just like
                  many other components, there are counterfeit sensors around
                  which have had early life failures.  
  
OK, assuming that the sensor is reading correctly,
                  let’s look at the settings required to set it up correctly.
                  Firstly, we highly recommend enabling the “trim for fuel
                  density” setting in Outputs -> Fuel System. This causes the
                  ECU to calculate the fuel density based on the measured fuel
                  temperature and also the ethanol percentage, and use that to
                  convert the fuel mass calculation into a volume, to calculate
                  the injector duration required.  
  
![11_trimfuel](../images/028_FlexFuel/11_trimfuel.png)![12_intermediate](../images/028_FlexFuel/12_intermediate.png)  
  
Next, for the fuel map that you’re using (we’ll
                  assume you’re using fuel map 1), we need to change the Stoich
                  source from “constant” to “flex fuel”. This means that instead
                  of using a fixed stoichiometric ratio, the ECU will look at
                  the ethanol percentage from the sensor and calculate the
                  stoichiometric ratio from that. The stoich value will be the
                  value that the ECU will use in the event of a sensor failure,
                  so for example if your normal fuel is E85 then you would put
                  10.0 in this setting.  
  
![13_fromflex](../images/028_FlexFuel/13_fromflex.png)  
  
The way the fuel calculation works is that you have
                  three tables. You have the basic VE table, the same as if you
                  were doing a fixed-fuel tune. Then there is a correction table
                  for 0% ethanol, and a second correction table for 85% ethanol.
                  The ECU interpolates between these two tables and uses this to
                  trim the main fuel map.  
  
![14_fuelcalc](../images/028_FlexFuel/14_fuelcalc.png)  
  
The first step is to then set both E0 and E85 maps
                  to zero.Then tune the first fuel on the main map.  
  
![15_fuel_1](../images/028_FlexFuel/15_fuel_1.png)  
  
Then switch to the second fuel, and modify the
                  correction map for that fuel so that the lambda is still
                  correct with the new fuel. In theory this map should be zero
                  everywhere; in practice the maps tend to be in the range of
                  ±5% usually. This method allows you to either tune E0 or E85
                  first.  
  
![17_fuelcalc_e85](../images/028_FlexFuel/17_fuelcalc_e85.png)  
  
![16_fuelcalc_e0](../images/028_FlexFuel/16_fuelcalc_e0.png)  
  
For ignition timing, the same process occurs where
                  you have the main ignition map, and then an E0 and an E85
                  correction map. If you use the E85 condition as the default
                  condition, then the E85 map will be zero and the E0 map will
                  have negative values in it to pull out timing at the lower
                  ethanol percentage.  
  
![19_2_e85](../images/028_FlexFuel/19_2_e85.png)![19_2-2_e85](../images/028_FlexFuel/19_2-2_e85.png)  
  
![18_1_petrol](../images/028_FlexFuel/18_1_petrol.PNG)![18_1-1_petrol](../images/028_FlexFuel/18_1-1_petrol.png)  
  
There is a third way that you can do ignition
                  timing, because the timing values are added – and that is to
                  leave the main ignition map at zero, and then you can treat
                  the E0 map as the ignition map for no ethanol, and the E85
                  correction map can be your ignition map for E85. The downside
                  is that the ignition correction maps are only 15×15 in size
                  instead of the main ignition map which is 31 x 31 but in
                  practice I don’t think this would be a limitation.  
  
![20_3_ignitionmap](../images/028_FlexFuel/20_3_ignitionmap.png)  
  
The final behaviour that can be affected by ethanol
                  percentage is boost. To enable this, go to the boost settings
                  page and select “limits”. Enable the “limit boost by ethanol
                  content” checkbox, and then select the limit vs ethanol
                  content. If you are in open loop, duty cycle mode, then this
                  table is a duty cycle limit for the wastegate actuator based
                  on the ethanol percentage. If you are in a target boost mode,
                  then these values become the new lower target boost when the
                  ethanol content is lower. Obviously the target boost or duty
                  cycle limit has to be higher than what you intend to run at
                  E85 at the 85% point, otherwise it will limit your boost.  
  
![21_ethanolpercentage](../images/028_FlexFuel/21_ethanolpercentage.png)  
  
![22_openloop](../images/028_FlexFuel/22_openloop.png)  
  
Also obviously when testing boost limit based on
                  ethanol, remember that other limits might be applying at the
                  same time, for example gear and external boost selection
                  inputs.  
  
One final point about flex fuel, the ECU “thinks” in
                  lambda rather than AFR. The AFR is only calculated as an
                  intermediate step in working out the fuel quantity from the
                  air quantity. So to avoid confusion and delay, we recommend
                  displaying lambda and using lambda targets, because firstly
                  that’s what the engine really cares about (that is, whichever
                  fuel you’re running, the target lambda is usually
                  approximately the same, certainly between ethanol and petrol)
                  and secondly that’s what the lambda sensor actually measures.
                  If you ask the software to display it as AFR instead of
                  lambda, it displays what we call “petrol AFR” which is lambda
                  multiplied by 14.7. This will not be the correct AFR unless
                  your stoichiometric ratio is 14.7. However, it seems that
                  almost all lambda sensors display lambda in this way by
                  default if not exclusively, and that also includes the lambda
                  / AFR displays on dynos.  
Thank you very much!  
©2018
        Adaptronic  
