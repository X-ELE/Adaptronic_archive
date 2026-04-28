Eugene Table and Graph How To's/*

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
  


How to Use Tables and Graphs

[go back to support
                home](EN_EUGENE_HOME.md)

![image](../images/Eugene/Eugene250.png)  


[Eugene basics  

              ](EN_EUGENE_ABOUT.md)

[Keyboard
                shortcuts for tables and graphs  

              ](EN_EUGENE_KBSC_TG.md)

  


[  

              ](EN_SelFW.md)

  


  
  

- [Setting up axes](EN_EUGENE_HOW_TABLE_GRAPH.html#Setting_up_axes)
- [Inserting cells](EN_EUGENE_HOW_TABLE_GRAPH.html#II._Inserting_cells)
- [Deleting cells](EN_EUGENE_HOW_TABLE_GRAPH.html#III._Deleting_cells_)
- [Selecting cells](EN_EUGENE_HOW_TABLE_GRAPH.html#IV._Selecting_Cells)
- [Data Entry](EN_EUGENE_HOW_TABLE_GRAPH.html#IV._Data_Entry)
- [Interpolation](EN_EUGENE_HOW_TABLE_GRAPH.html#V._Interpolation)
- [Duplicating
                      cell value a.k.a. Copy/Paste](EN_EUGENE_HOW_TABLE_GRAPH.html#VII._Duplicating_Cell_Values_a.k.a)
- [Map trace](EN_EUGENE_HOW_TABLE_GRAPH.html#VIII._Map_Trace)
- [Cell Tagging](EN_EUGENE_HOW_TABLE_GRAPH.html#IX._Cell_Tagging)[]()Setting
                    up the axes  
X and Y axes of the table may
                  have different data types depending on which settings you're
                  working on.. For example if you're working on a fuel map,
                  X-axis has the RPM data type while the Y-axis has either MAP
                  or TPS, depending on your load selection setup.  
  
1. To start setting up
                  the X-axis, right-click on the table (or graph) and choose
                  'Change X-axis step size' from the pop-out menu. The axis
                  configuration window will pop out.  
  
![changeaxis](../images/Eugene/TabGraph_ChangeAxis.png)  
  
2. You should be able
                  to insert and delete entry points in the axis range, or set
                  the maximum axis value and Eugene will work out each interval
                  in the series. This fills out the maximum number of columns
                  for X-axis (or rows for Y-axis).  
3. Once everything is
                  set, click OK. If an error is detected (e.g. duplicate
                  netries, etc), fix the entry value and hit OK again.  
  
[Back to
                    top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Inserting
                    cells  
Inserting a row
                  or column is easy!  
  
1. Click on the table
                  to select a cell.  
2. HitINSERTkey to insert a column (orSHIFT
                    + INSERTto insert a row).  
3. A window will pop
                  out to ask for the Column (or row) header value. The default
                  value is usually the average between the activell cell column
                  and the column to the right (or the active cell row and the
                  row below).  
![insertcell](../images/Eugene/TabGraph_InsertCell.png)  
4. Hit OK when
                  finished.  
  
[Back to
                    top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Deleting cells  
Deleting cells are
                  much easier! Unlike inserting cells, you can delete multiple
                  columns or rows at one time.  
  
1. Click (and drag) to
                  selec the columns or rows to be deleted.  
2. HitDELETEkey to delete columns (orSHIFT
                    + DELETEto delete rows).  A prompt window will
                  pop out for the confirmation.  
3. Hit YES to confirm.  
  
[Back
                    to top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Selecting Cells  
Navigating through the
                  cells can be done by using mouse or arrow keys.  

- To select multiple
                      cells, simply select the starting cell and then hold downSHIFTkey while
                      using the arrow keys. When using a mouse, simply drag
                      while pressing left-mouse button.
- Selecting the
                      entire column or row is done using a mouse by clicking on
                      the header. To select multiple columns or rows, just drag
                      from the initial header while pressing left-muse button.[Back to
                    top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Data Entry  
Only these are valid
                  entries in data tables  

- Numbers 0-9
- Decimal point ( .
                      )
- Negative sign (
                      - )  
After entering the
                  number, hit ENTER key so Eugene can validate the entry ie
                  checking within the preset minimum and maximum value. If an
                  ECU is connected (online) the new values in the table are then
                  written into the ECU.  
  
Tips:  
a. To invalidate
                      an entry, press ESCAPE key to revert to previous cell
                      value  
b. To increment /
                      decrement the cell's value, press PAGE UP or PAGE DOWN.
                      When pressed while holding CTRL key down, the increment or
                      decrement is the tenth of the default increment value  
  
[Back
                    to top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Interpolation  
Use the interpolation
                  function to blend parts of the map. There are 3 ways to do it:  
  
1.
                  Interpolate from Corner  
a.
                  Select group of cells (at least 3x3) in the table. To
                  select all cells, pressW(Select All).  
b.
                  PressLto start
                  interpolation  
2.
                  Interpolate Columns  
a.
                  Select group of cells (at least 3 cells in a column) in
                  the table. To select all cells, pressW(Select All).  
b.
                  PressYto start
                  interpolation  
3.
                  Interpolate Rows  
a.
                  Select group of cells (at least 3 cells in a row) in the
                  table. To select all cells, pressW(Select All).  
b.
                  PressXto start
                  interpolation  
  
[Back to
                    top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Duplicating
                    Cell Value a.k.a Copy/Paste  
There are two ways to do
                  it  
  
1.
                  Conventional Copy and Paste  
a.
                  Select a cell or group of cells to be copied and then pressCTRL + C.  
b.
                  Click on the cell where you want those values to be copied and
                  then pressCTRL + V.  
  
Note: If the size of the copied cells is 3x3 for example,
                  it will be pasted to a 3x3 cell area as well.  
  
2.Speed
                    Copy- this mode copies the active cell value to its
                  adjacent cell. This mode needs to be activated though by
                  pressingD.  
a.
                  Copy single cell - click on the cell that will be copied, and
                  then pressCTRL + ARROWkeys to start copying.  
b.
                  Copy entire column - click on the column header, and then
                  pressCTRL + LEFT/RIGHT
                    ARROWkey to start copying.  
c.
                  Copy entrire row - click on the row header, and then pressCTRL + UP/DOWN ARROWkey
                  to start copying.  
  
[Back to
                    top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Map Trace  
This function is only
                  available when an ECU is connected and Eugene is reading gauge
                  data out of the ECU. When this happens, the cross hair in the
                  table will be shown, displaying the the axes' live data values
                  from the ECU. Map trace function basically just maps out the
                  cells that were previously active based on the axes' live
                  data.  
  
When this function is
                  enabled (by pressingT), the active cells (both
                  previous and current) are highlighted in color RED, except for
                  fuel map tables which highlights are based on the
                  leanness/richness of the average AFR vs. the target AFR.  
  
![maptrace](../images/Eugene/TabGraph_MapTrace1.png)  
  
[Back to
                    top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
[]()Cell
                  Tagging  
When working with fuel
                  maps, a cell can be tagged as "Tuned" or "Untuned".  
  
1. Select cells to be
                  marked, either by using a mouse or by arrow keys.  
2. PressMto mark cells as'Tuned"or pressUto mark cells as "Untuned".  
3. Tuned-marked cells
                  will have a green font color to be distinguished among the
                  rest.  
  
![marktuned](../images/Eugene/MarkTuned.png)  
[Back to
                    top](EN_EUGENE_HOW_TABLE_GRAPH.html#top)  
  
©2018
        Adaptronic  
