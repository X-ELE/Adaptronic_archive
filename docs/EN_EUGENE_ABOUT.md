Eugene Basics/*

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
  


Eugene Basics

[go back to support
                home](EN_EUGENE_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Manipulating tables and graphs  

                ](EN_EUGENE_HOW_TABLE_GRAPH.md)

[Keyboard
                  shortcuts (Main)](EN_EUGENE_KBSC_MAIN.md)

[Keyboard
                  shortcuts (tables)  

                ](EN_EUGENE_KBSC_TG.md)

[Navigating
                  Eugene menus](EN_MOD_002_HOMERIBBON.md)

[The
                  Gauge Page](EN_EUGENE_GAUGE_PAGE.md)

[Adding a custom gauge  

                ](EN_EUGENE_GAUGE_PAGE.html#Adding_custom_gauges)

[  

              ](EN_SelFW.md)

  


  
  
  
[]()Eugeneis the Engine
                  Management Software designed forAdaptronic
Modular
                  ECUs. It is also
                  compatible withAdaptronic Select ECU models.
- [Starting
                      Eugene](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_EUGENE_ABOUT.html#Starting_Eugene)
- [Navigating the menu](EN_EUGENE_ABOUT.html#Navigating_the_Menu)
- [Status Bar](EN_EUGENE_ABOUT.html#Status_Bar)
- [Monitor Panel](EN_EUGENE_ABOUT.html#Monitor_Panel)
- [Gauges
                        Window](EN_EUGENE_ABOUT.html#Gauges_Window)
- [](EN_EUGENE_ABOUT.html#Gauges_Window)[ECU
                      Data](EN_EUGENE_ABOUT.html#ECU_Data)
- [](EN_EUGENE_ABOUT.html#Gauges_Window)[Gauge
                      Page](EN_EUGENE_ABOUT.html#Gauge_Page)
- [Simulator (Modular)](EN_EUGENE_ABOUT.html#Simulator)[]()Starting
                      Eugene  
  
Double-click "Launch
                      Eugene" icon from Desktop.  
  
![eugene image](../images/Eugene/Splash_screen.png)  
  
The user can either
                      load the settings (1) by opening a basemap (.ECU
                      file) or (2) by connecting an ECU via USB or Wi-Fi.  
  
When an ECU is connected
                      via USB, the software can communicate and retrieve
                      the settings even there is no 12V ignition power
                      going to the ECU. (This is possible due to the 5V power
                      inside a USB cable)  
  
Now, with Eugene running
                      and the ECU connected, the user should verify that the
                      software can see the ECU. A message such as 'ECU
                        connected’ or ‘Reading
                        Settings’, rather than‘No
                        ECU connected’ should be displayed. The status
                      should then progress from‘Reading
                        Settings 0%’ to ‘Reading
                        Settings 100%’ as the settings are extracted from
                      the ECU.  
  
[](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_EUGENE_ABOUT.html#top)[Back
                    to top...](EN_EUGENE_ABOUT.html#top)[](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_EUGENE_ABOUT.html#top)[]()Navigating
the
                  Menu  
  
For detailed instructions,
                  click[here](EN_MOD_002_HOMERIBBON.md)[.](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_EUG_NAV.md)  
  
The Ribbon menu is laid out
                  logically in the order the user would set things up in the
                  ECU. The Home menu tab has the access to all  functions
                  and tools for convenience in using the software. The rest of
                  the menu tabs are the groups of settings that the user would
                  setup, as outlined at the home page.  
  
![home menu](../images/Eugene/Home_Menu.png)  
  
File  

- Open ECU File-
                    allows the user to load ECU settings from a file (*.ecu)
- Save As-
                    save current settings into a file with a specific file
                    name
- Save- save current
                    settings to the active file name
- Import- import
                    specific settings or tables from another ECU fileUnits  

- Pressure- toggles
                    unit for Pressure, i.e. kPa or inHg/psi
- Temperature-
                    toggles unit for temperature, i.e. °C or °F
- Fuel Ratio- toggles
                    unit for fuel ratio, i.e. AFR or Lambda
- Speed- toggles unit
                    for vehicle speed, i.e. km/h or mi/hTools
and
                    Config  

- Software settings - access the rest of the settings
                    in the software, e.g. Communications Port, table axis
                    orientation, etc
- Read All - read all settings from the ECU
- Write All - write all settings to the ECU
- Update FW -  flashing new FW for the ECU
- Comm. Port - selection on where the ECU is connected
- Lock ECU - only for Modular. Disables any write
                    events going to the ECU
- Optimize - only for Modular. Optimizes settings
                    synchronization between Eugene and ECUPage Mode-
                    toggle between Classic and Custom Page mode  

- Classic - can only view one table or settings config
                    window at a time. Full access to the monitor panel
- Custom Page - can view multiple table / settings
                    config window in one page. No access to monitor panel (gauge
                    displays can be added on the same page)Quick link to maps  

- shortcut access to
                      active fuel and ignition mapsLogging  

- Start Logging (Ctrl + L) - initiates the log session.
                    Eugene creates two files, Adaptronic Log file (.alg) and a
                    Comma-Separated Values file (.csv)
- Stop Logging (Ctrl + K) - ends logging session
- Log Converter - tool used to convert .ALG log file to
                    .CSV
- CSV Log Channels - only for Modular. Allows user to
                    select which live channels in ht eModular are to be logged
                    in CSV format. ALG files on the other hand logs all
                    live channels
- Log Viewer - access to Adaptronic Log Viewer, and
                    opens the most recent log created in the session. If there
                    are no recent log, it will ask the user to select a log fileReference  

- allows the user to
                      open the wiring document and pinout guide for the current
                      ECU modelContact  

- opens a window
                      that will allow users to create an email (with file
                      attachments) to Adaptronic Technical Support
                      (tech@adaptronic.com.au)  
[Back
                    to top...](EN_EUGENE_ABOUT.html#top)[](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_ABOUT_EUGENE.html#top)[]()Status Bar  
  
![statusbar](../images/Eugene/status_bar.png)  
  
A.
                    Locked/Unlocked - only for Modular. Displays "ECU Lock"
                    state.When
                    an ECU is locked, the user can not write/modify any settings
                    in the ECU. To Lock/Unlock, click on "Lock
                      ECU" in "Tools and
                      Config" underHomemenu tab.  
B. Connection Status -
                    displays current ECU connection status. When an ECU is
                    connected, the serial number and FW version is also
                    displayed. Also indicates Read/Write progress  
C. Timing Locked -
                    when RPM > 0 and the timing locked is set in the
                    settings, this indicator will blink  
D. Fuel Cut -
                    indicator if the ECU is in Fuel cut  
E. Ignition Cut -
                    indicator if the ECU is in Ignition cut  
F. Search - access to
                    Search window, which allow the user to search for specific
                    setting in config window or tables.Shortcut key: Ctrl + F  
  
[Back
                    to top...](EN_EUGENE_ABOUT.html#top)[](EN_EUGENE_ABOUT.html#top)[]()Monitor Panel(Ctrl
                  + F2)  
  
An area in the main
                    window that allows users to add gauge displays to view live
                    variables that are being monitored.  
There are two monitor panels in Eugene main window: (1)
                    static and (2) dynamic  
  
1.
The
                      static monitor is the upper portion of the panel, where
                      gauge displays are constantly visible regardless of the
                      changes in the settings configuration window or tables.
                      Usually gauge display of basic live variables (e.g. Engine
                      speed, MAP, Throttle position, etc) are found here since
                      they're mostly likely being monitored throughout the
                      entire tuning process.  
  
2. The dynamic
                      monitor is the lower portion of the panel, where
                      the gauge displays are relevant to the active
                      settings configuration / table window being shown.  
  

- [How
                      to add a gauge display in the Monitor panel](EN_EUGENE_GAUGE_PAGE.html#Adding_custom_gauges)
- [Learn more about
                      the Monitor panel](EN_EUGENE_GAUGE_PAGE.md)  
  
[Back
                    to top...](EN_EUGENE_ABOUT.html#top)[](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_ABOUT_EUGENE.html#top)  
[]()Gauges
                      Window (F2)  
  
Displays all (available)
                      live channels for monitoring.  
With Modular, some live
                      channels (e.g. Engine Speed) have its target and effort
                      values displayed inside the parenthesis:  (Target
                      value  |  Effort value)  
![F2window](../images/Eugene/F2_Window.png)  
  
  
[Back
                    to top...](EN_EUGENE_ABOUT.html#top)[](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_ABOUT_EUGENE.html#top)[]()ECU Data (F11)  
  
Displays control board's
                      live voltages and output overrides (Modular).  
  
![modecudata](../images/Eugene/Mod_ECUData.png)  
  
[Back
                    to top...](EN_EUGENE_ABOUT.html#top)[](file:///C:/Users/Frank/Dropbox/Release/Support/EN/EN_ABOUT_EUGENE.html#top)[]()Gauge Page (F3)  
  
A page dedicated for custom
                  gauge displays.  
For users who are running
                  Eugene in a tablet dash, it's highly recommended to set the
                  start-up view to "Full-screen gauge page Mode" (see Software
                  Setttings -> Misc.)  
  
![gagugepage1](../images/Eugene/GaugePage1.png)  
  

- [How
                      to add a gauge display in gauge page.](EN_EUGENE_MONITOR_PANEL_GAUGE_PAGE.md)
- [Learn more about
                      the Gauge page](EN_EUGENE_GAUGE_PAGE.md)  
[Back
                    to top...](EN_EUGENE_ABOUT.html#top)[]()Simulator (F7) - Modular  
  


Allows the user to simulate
                  most of the live values, replicate almost any real-world
                  situation, and observe the behaviour of the ECU settings (no
                  need for the ECU to be connected!)

We strongly recommend
                  testing any setting changes using this simulator whenever
                  possible!![simulator](../images/Eugene/Mod_Simulator.png)  
  
  
[Back
                        to top...](EN_EUGENE_ABOUT.html#top)  
  
  
  
©2018
        Adaptronic  
