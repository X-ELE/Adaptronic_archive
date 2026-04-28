Fuel Model in Modular ECUs/*

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
  


Fuel Model in Modular ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Different
                Fuel Tuning Modes](EN_MOD_027_FUELTUNINGMODES.md)[ ](EN_EUGENE_ABOUT.md)

[How
                Fuel Mass is Converted to Milliseconds  

              ](EN_MOD_032_INJECTORMODEL.md)

  


[  

              ](EN_SelFW.md)

  


  
  
[](https://youtu.be/I-9FW3VrxEI)  
  
  
Hello all, in this article I’ll describe the fuel model in the
                Modular ECUs. This is based on a talk that I gave at PRI in
                2016, but in this talk I’ll talk specifically about where the
                settings are for the Modular ECU. In this talk I’m only talking
                about steady state tuning. However you need to understand this
                to be able to learn about transient fueling, and injector
                modelling. So if you like this is the first part of my PRI talk,
                but with specific reference to the Modular ECU settings.  
  
We’ve all seen the famous Greg Banish, Calibrated Success
                T-shirt which you can buy from Summit Racing, and I’m wearing
                mine now actually. I’m not sure I understand whether Mr Banish
                was expressing frustrating saying that it’s simple, why don’t
                people understand it – or if he’s making a joke and saying that
                actually there are many different terms in this equation, and if
                you don’t understand them all then you can get lost quickly. But
                either way, if it looks intimidating to you now, you’ll
                understand it in about twenty minutes so don’t worry.  
  
![1_Tshirt](../images/029_FuelModel/1_Tshirt.JPG)  
  
Let’s talk firstly about the way that we and other ECU
                manufacturers used to do things, and hopefully you’ll see why
                we’ve changed to a proper fuel model now. Firstly, what is the
                purpose of the injector control in the ECU? It’s to get the
                right amount of fuel into the engine, to achieve a particular
                lambda…. when the tuner isn’t there to correct it! That means
                that we’re trying to control the injectors and deal with all the
                different conditions that will occur that will affect the
                lambda, if we don’t care about them.  
  
The fuel requirement of an engine varies mostly with manifold
                pressure, and to a lesser extent it varies with RPM. The obvious
                way is therefore to have a table of millisecond values as a
                function of both MAP and RPM, and we’d call this a fuel map. And
                this works quite well, so long as all the other variables are
                constant.  
  
So which variables are not included in this calculation, and
                we’re assuming are constant, but actually are not constant? When
                I did this at PRI I let people call them out and I threw Tim
                Tams to people who answered, but I can’t do this here so I’ll
                just tell you the list I came up with:  

- Temperatures – coolant, air, fuel
- Fuel pressure
- Battery voltage
- Fuel composition (ethanol vs petrol)
- Injector type  
Now, I realise that the Injector Type isn’t really a variable,
                because it’s supposed to be something that’s installed on the
                car before you do a tune. And there is some case to say that it
                would be nice to be able to change injectors and not have to do
                a complete return. But that’s not the main point. The main point
                is that often tuners tend to specialise in particular engine
                types, and end up developing a decent library of maps for these
                engines in which they specialise. However often they don’t get
                to choose the injectors on the engine when they have to tune it,
                so they don’t get to use one of their maps from their library
                because the milliseconds are all wrong.  
  
So to deal with these variables, what ECU manufacturers
                (including us) used to do is to add in “compensation tables” for
                all of these variables. For example to deal with battery voltage
                changes, old ECUs had a “battery voltage compensation table”
                where you could enter a number of milliseconds to add to the
                injector duration as a function of battery voltage.  
  
Now, as a tuner, how do you know how to set this table? How many
                tuners are going to run the EFI system off a variable power
                supply and wind it up and down, adjusting the table so that the
                AFR at idle is constant? I don’t know many tuners who would do
                that.  
  
Similarly for temperature changes, you have separate tables for
                coolant temperature and air temperature, which makes life very
                complicated. How do you know if it’s the air or the coolant
                table which is wrong, for example? In general the more
                correction tables that you have, the harder it is to know which
                table needs to be adjusted, and the longer it takes. And to be
                honest, if you have all these compensation tables to account for
                incorrect assumptions you’ve made about other variables being
                constant, maybe your model isn’t that good in the first place.
                As in, maybe having a millisecond map against RPM and MAP isn’t
                the right way to do it.  
  
So let’s go back to chemistry and physics and work it out from
                first principles instead of making these assumptions.  
  
![Slide14](../images/029_FuelModel/Slide14.JPG)  
  
This is just the definition of an Air-Fuel ratio, and the
                definition of Lambda.  
  
![Slide15](../images/029_FuelModel/Slide15.JPG)  
  
The top one is called the Ideal Gas Equation or Boyle’s Law, and
                it’s given by the pressure times the volume equals the number of
                moles times the ideal gas constant times the temperature. Note
                that the pressure and temperature in this equation are absolute
                temperature and pressure.  
  
The second one is the conversion between number of moles into
                mass, based on the molecular weight of the gas. A mole is
                defined as approximately 6.022 x 10^23 molecules in this case.
                We don’t count the molecules, we just work it out from the
                weight and knowing what air is made of.  
  
![Slide16](../images/029_FuelModel/Slide16.JPG)![Slide17](../images/029_FuelModel/Slide17.JPG)  
  
This is the definition of volumetric efficiency. It’s given by
                that Greek letter Neta, which looks like n, which is the
                thermodynamic symbol for efficiency, and it’s given by the ratio
                of the effective volume of air that travels through the inlet
                valve into the cylinder, if it was the same pressure as in the
                manifold, divided by the swept volume of the cylinder. In
                practice of course the volume expands or compresses to fit in
                the cylinder anyway, so it’s the pressure that changes, not the
                volume, but volumetric efficiency is a way to think of it.  
  
![Slide18](../images/029_FuelModel/Slide18.JPG)![Slide19](../images/029_FuelModel/Slide19.JPG)![Slide20](../images/029_FuelModel/Slide20.JPG)![Slide21](../images/029_FuelModel/Slide21.JPG)![Slide22](../images/029_FuelModel/Slide22.JPG)![Slide23](../images/029_FuelModel/Slide23.JPG)  
  
You can see now that we’ve essentially arrived at Greg’s T-shirt
                equation. There’s a scaling difference of 1000 in there, so I
                assume that’s because he’s calculating fuel in grams instead of
                the SI unit of kg or something like that.  
  
Now, let’s go over all the variables again and see how we can
                measure or know what they are.  
  
Mfuel is what we’re trying to calculate  
  
MAP is something that we can measure directly with a MAP sensor.
                To learn more about how you can measure this accurately, see the
                video on configuring inputs because there are some funky
                requirements regarding filtering, because the MAP is not
                constant throughout a cycle.  
  
VE is something we can look up from the fuel map. This replaces
                our millisecond fuel map. Please see my tuning modes video for a
                more detailed discussion of VE, what affects it on different
                types of induction systems.  
  
Vcyl – cylinder volume, the ECU knows this at setup time because
                of the engine capacity and number of cylinders.  
  
T – the air temperature, is taken as a blend between air and
                coolant temperature; I’ll do a separate article just on that
                topic.  
  
Lambda, is the lambda that we want, so that just comes from the
                target lambda table  
  
AFRstoich comes either from an ECU setting, or is calculated
                from measurement from a flex fuel sensor.  
  
![Slide25](../images/029_FuelModel/Slide25.JPG)  
  
There should be some implications of this formula. For example
                if you double the manifold air pressure, then all other things
                being equal, the amount of fuel you need to inject every intake
                stroke will approximately double. Sometimes people ask questions
                like “why does the VE map look so flat, why doesn’t it increase
                a lot with boost”, but it should be obvious when you see this
                formula.  
  
Another question we get asked is, if I change the target lambda,
                will the ECU change the amount of fuel injected. And again, you
                can see from this formula that the answer is yes.  
  
This formula also means that in theory, your temperature
                correction maps should be zero, because they are supposed to be
                handled by the formula. And in practice, I have always left them
                at zero so far, and it works well because the model is accurate.  
  
Let’s look now at how this is all set up in the ECU. There are
                separate videos / articles on each of these topics so I’ll just
                tell you where all the settings are here.  
  
Engine capacity and number of cylinders (or rotors) are both set
                up in Engine -> Details.  
  
![2_engcap_cyl](../images/029_FuelModel/2_engcap_cyl.png)  
  
The stoich AFR is set up in the fuel map settings, for example
                Tuning – Fuel -> Basic Setup –Fuel Map 1 Settings. This
                location also allows you to set how the VE fuel map is
                configured, and also where the VE mode setting is located.  
  
![3_afr](../images/029_FuelModel/3_afr.png)  
  
There’s another article specifically about tuning modes, how to
                set up the load axis for fuel maps based on the type of
                induction system on the engine.  
  
![4_loadaxis](../images/029_FuelModel/4_loadaxis.png)  
  
Target lambda can be found in Tuning-Fuel -> Target Lambda  
  
![5_targetlambda](../images/029_FuelModel/5_targetlambda.png)  
  
The temperature is taken from the coolant and air temperature
                sensors. By default, we use the manifold heat soak % mode which
                uses a blend of the two. This is enabled in the Tuning-Fuel
                -> Basic Setup -> Tuning Modes page, and the heat soak
                percentages can then be found in the Tuning-Fuel ->
                Temperature Correction -> Manifold Heat Soak %. This is the
                amount of weight to give to the coolant temperature, eg 100%
                means that there’s so much heat soak that by the time the air
                gets into the engine, its at engine temperature and the original
                air temperature doesn’t matter at all. 0% heat soaks means that
                there’s no effect on the air temperature by the engine
                temperature at all, which never happens in practice.  
  
![6_heatsoak](../images/029_FuelModel/6_heatsoak.png)  
  
![6_table](../images/029_FuelModel/6_table.png)  
  
MAP and temperature inputs are configured in the Inputs menu,
                and there’s other article that talks about those specifically.  
  
![7_inputs](../images/029_FuelModel/7_inputs.png)  
  
This doesn’t get you all the way to the injector millisecond
                value though, it gets you to the fuel mass. There’s a separate
                article on this, which includes the injector model, minimum
                pulsewidth or fuel delivery, the effects of fuel pressure and
                fuel temperature and so on. This also does not discuss transient
                conditions which is done in another article.  
  
Finally, the ECU reports a lot of its intermediate calculated
                values. So you can see things like the actual VE read from the
                table, and the calculated stoichiometric AFR, the calculated
                charge temperature and so on by going to the gauges window and
                expanding the “intermediate calculated value” section.  
  
![8_intermidiate](../images/029_FuelModel/8_intermidiate.png)  
  
You can also see this diagrammatically by going to the
                Diagnostics -> Calculation Trace.  The main fuel display
                shows the whole fuel calculation which is quite large, but you
                can click on individual sections in it to go into more details
                of the calculation. This also works with the software simulator.  
  
![9_calctrace](../images/029_FuelModel/9_calctrace.png)  
Thank you!  
©2018
        Adaptronic  
