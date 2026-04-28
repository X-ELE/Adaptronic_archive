Adaptronic Logviewer Help/*

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
  


Adaptronic Logviewer

[go back to support
                home](EN_EUGENE_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Eugene
                Basics  

              ](file:///C:/New%20Help/EN_EUGENE_ABOUT.md)  


[  

              ](EN_SelFW.md)

  


  
  
  

- [Features](EN_EUGENE_LOGVIEWER.html#I._Features:)
- [The
                        Main Workspace](EN_EUGENE_LOGVIEWER.html#II._The_Main_Workspace:)
- [The Flag Display Tab](EN_EUGENE_LOGVIEWER.html#III._The_Flag_Display_Tab)
- [The
                        Channel and Flag Selection Screens](EN_EUGENE_LOGVIEWER.html#IV._The_Channel_and_Flag_Selection)
- [Keyboard
                        Shortcuts](EN_EUGENE_LOGVIEWER.html#V._Keyboard_Shortcuts:)  
[]()Features:  

- The Adaptronic log viewer is cable of displaying
                    files created with Eugene (ALG files), WARI (CSV files), and
                    SEKUKU (CSV files).
- ALG files contain all the information available to
                    the user, except ones made with internal logging for space
                    saving reasons.
- The log viewer graphs in a time-based manner instead
                    of  a "log based" manner., meaning even if there is a
                    discrepancy in the interval of logging (which is the case
                    since logging is dependent on clock cycles instead of a
                    fixed time interval), the graphing is still accurate vs.
                    time.
- ALG files also contains the ECU information when
                    the log was taken. This makes diagnosis a lot easier for you
                    or us.
- CSV extraction is useful if you want to view the file
                    usng spreadsheet software of other log viewers
                    available.
- Because if the endless possibilities of the number
                    channels that can be displayed with CSV files, there is no
                    default channel setting. The channels window will
                    automatically appear the first time you open a CSV file.
- With Modular ECUs, flags are saved as well, and you
                    can view these with the log viewer, again making diagnosis
                    easier.![Extractcsv](../images/Eugene/Export.png)  
Modular ALG (Recorded
                        with Eugene)Select ALG File
                        (Recorded with Eugene)CSV File (Recorded
                        with WARI or converted)Unit ConversionYESYESNOFlagsYESNONODisplay Target ChannelYESYESNOConversion to CSVYES*YES*N/ACustom RangeYESYESYES*Unlike Eugene, only
                  channels flagged as favorites will be written into the CSV of
                  the same filename, located in the same folder.[]()The Main Workspace:  
![Main workspace screenshot](../images/Eugene/Main.png)  

- Navigation - Drag the mouse with the left
                    button over the navigation bar to select the area to display
                    on the main window. Navigation parameter can be changed in
                    the channels window. Zoom in/out by pressing PageUp/Dwn or
                    clicking the Zoom Button, visible if the mouse hovers in the
                    area between the two cursors. Navigate left or right using
                    the left/right arrow keys or drag the scroll bar below the
                    graphing area.
- View - You can hide/show the Navigation bar and
                    Bottom Panel by clicking the shown buttons or pressing the
                    up or down arrow key. You can also drag the bottom panel
                    upwards or downwards by pointing in the area below the
                    scrollbar.
- Range labels - You can approximate the actual value
                    with these labels. There are 10 "steps", with interval of
                    maximum (denoted) minus minimum over 10. You can customize
                    the minimum and maximum using the Channels window.
- Cursors -There are two cursors, Cursor 1 is
                    positioned with a left click on the workspace, Cursor 2 with
                    a right click. Actual graph values are displayed at the
                    table located at the bottom of the screen. Each column is
                    described below in the next section.
- Time Display/Button - Can either show the time
                    difference of the position of both cursors or the exact time
                    the selected cursor is pointed to. Simply left click to
                    change mode. (Note: Each vertical "line" in the graph may be
                    representative of a time range. Thus the displayed value is
                    the average value of all the logs made in that range)
- Bottom Panel - Contains a table that displays
                    numerical values based on the positions of the two cursors
                    and controls which channel and it's target (if applicable)
                    is visible. Clicking on a row description (parameter name)
                    will display the Channels window wuth that parameter
                    selected.
- Cursor 1/2 Value - Displays the scaled value of each
                    parameter in the current position of the cursor.
- Delta - The difference of the values of each
                    parameter (ie. how much it has changed from cursor 1 to 2).
- Delta Rate - The rate divided by the time elapsed
                    between cursors.
- Minimum - The minimum value in the area between
                    cursors.
- Maximum - The maximum value in the area between
                    cursors.
- Cursor 1/2 error - Only applicable in channels with
                    targets. Shows the difference between a parameter and it's
                    target value. (ie. Closed loop)[]()The
                  Flag Display Tab  
![flagsimage](../images/Eugene/Flag.png)  

- Only Cursor 1 is used in flag selection. The
                    background color of the graph row label becomes red if the
                    flag is active when the cursor is over it. Parameters at the
                    bottom are displayed as usual. Cursor 2 does not detect of a
                    flag is active or not, but still shows the associated values
                    in the bottom panel.
- Navigation in this tab is much like main panel
                    navigation. In fact, you can just switch tabs since the
                    displayed time interval is the same.
- The flag tab is only available for Modular ALG logs
                    only. Not all flags are available in internal logs (only the
                    ones under FLAGSH and FLAGSL are logged every time
                    internally by default).[]()The Channel
                  and Flag Selection Screens:  
![Channels](../images/Eugene/Channels.png)  

- The left pane shows all the channels that have been
                    logged in tree form. Searching for a specific parameter
                    works too. Simply type on the text box and the tree will
                    expand to suit.
- Clicking the >> button or double clicking the
                    parameter will transfer it to the right pane, making it a
                    favorite.What are favorites?These are parameters
                      which are saved and flagged as ones to be loaded into
                      memory for later viewing. With 1024 channels, and a VERY
                      long log, not loading everything will save file
                      opening times. This is useful for opening files over a
                      network, etc.
- Checked channels in the right pane will select it for
                    viewing.
- To set the navigation parameter to use, simply click
                    "Use as Navigation Channel" with the channel selected. The
                    default is RPM.
- Channel graphing color, Custom minimum, maximum
                    (graph range)m Y-offset and Graph Height is saved per
                    channel.
- Units are saved globally, meaning setting it to °F
                    will convert, graph and display all temperature logs in that
                    unit.
- The Flag Selection screen has the same structure, but
                    does not have per channel settings.[]()Keyboard Shortcuts:  

- Left Arrow Key- Pan Graph to the left.
- Right Arrow Key- Pan Graph to the right.
- Up Arrow Key- Toggle navigation bar.
- Down Arrow Key- Toggle data table.
- Page Up-
                    Zoom to area between cursors.
- Page Down-
                    Zoom out.

[Back to top](EN_EUGENE_LOGVIEWER.html#top)©2018
        Adaptronic  
