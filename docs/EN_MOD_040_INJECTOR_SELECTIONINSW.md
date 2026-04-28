  
  
  
  
  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  
  
  
  
  
  

Selecting Injectors for the Modular ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)  

![image](../images/Eugene/Eugene250.png)
  
  
  

[How
                Fuel Mass is Converted to Milliseconds](EN_MOD_032_INJECTORMODEL.md)[
              ](EN_EUGENE_ABOUT.md)

[Injection
                Timing on Port Injected Engines  

              ](EN_MOD_035_INJECTORTIMING.md)

  

[  

              ](EN_SelFW.md)

  

  
  
  
  
  
  
  
  
  
In previous articles, I’ve said that
                  you can select your injector from a dropdown list. There are
                  currently 60 injectors in the list, so I thought it would be
                  appropriate to show some options to find your injector and
                  what other information you can gain from the injector
                  selection screen.  
  
Firstly, the injector selection can be found under
                  “outputs -> injector type” screen. The Modular ECUs
                  currently support up to 4 stages of injection and you can
                  select a different injector type for each stage. So each stage
                  has its own injector selection screen.  
  

![1_injtype](../images/040_Injector_SelectionInSW/1_injtype.png)
  
  

![2_4stages](../images/040_Injector_SelectionInSW/2_4stages.png)
  
  
Rather than searching through the list, you can
                  click on the “Search…” button next to the dropdown list. This
                  brings up a list of all the injectors we have characterised so
                  far, but as I mentioned it would be painful to search through
                  all of them. So instead it might be easier to do a search.  
  

![3_searchbutton](../images/040_Injector_SelectionInSW/3_searchbutton.png)
  
  
For example if you know that the injector is a
                  factory Nissan injector, you can type “Nissan” into the search
                  bar, and all the Nissan injectors we’ve characterised so far
                  will appear. The application for each (ie where we’ve found
                  them – they may be in other engines or cars as well) is shown,
                  and it also shows what we call the nominal flow rate. This
                  isn’t what we’ve measured, it’s just how people refer to them
                  colloquially so that if you know what your injectors are
                  called by people in the community, you can verify it in this
                  nominal flow field. The standard fuel pressure in the factory
                  vehicle is also shown in the nominal flow field.  
  

![4_typenissan](../images/040_Injector_SelectionInSW/4_typenissan.png)
  
  
To further help in identifying the injector, the
                  software shows the manufacturer’s markings on the injector,
                  both the manufacturer’s name and the part number. So if you
                  have some number on the injector, for example 2460 on the RX7
                  primary injector, you can type this into the search field and
                  see the injector appear in the search results.  
  

![5_2460](../images/040_Injector_SelectionInSW/5_2460.png)
  
  
Of course a really useful way to identify an
                  injector is by a picture, so we show a picture of the injector
                  as well.  
  
The dimensions of the injector are also shown, in
                  terms of the nominal length (usually 60, 48 or 34mm) and the
                  top o-ring diameter (14 or 11mm) – or it will just say “side
                  feed” if it’s a side feed injector.  
  

![6_dimension](../images/040_Injector_SelectionInSW/6_dimension.png)
  
  
Some other fields include the connector type, the
                  factory fuel system (manifold referenced or fixed fuel
                  pressure), and the person we need to thank for providing the
                  injector to characterise. If we have a serial or batch number
                  for the injector that we tested then that’s also shown.  
  

![7_columns](../images/040_Injector_SelectionInSW/7_columns.png)
  
  
Another field shown is the minimum volume. This is
                  the minimum volume of fuel that in our estimation the injector
                  can reliably deliver. With some injectors, below this volume
                  they just don’t deliver fuel accurately, for example the curve
                  has a very steep slope – or worse, if the injector is
                  underdamped you’ll see oscillations in the fuel volume so a
                  lower pulsewidth can cause an increase in the fuel delivered.
                  We want to keep away from such conditions, so this field shows
                  the minimum volume that you can expect from the injector at
                  the rated fuel pressure.  
  

![8_minfuel](../images/040_Injector_SelectionInSW/8_minfuel.png)
  
  
If you select a particular injector and click “OK”,
                  this will take you back to the main injector selection screen.
                  You’ll notice now that the settings for the flow rate and
                  offset / dead-time are no longer visible because they are hard
                  coded in the injector database in the ECU. A summary of the
                  information from the search screen is also shown on this
                  screen for your reference.  
  

![9_ok](../images/040_Injector_SelectionInSW/9_ok.png)
  
  
After this we’d recommend setting the minium
                  pulsewidth to zero, and setting the minimum fuel volume
                  setting to the value displayed in the summary at the bottom.
                  The reason we don’t do this automatically is that we know some
                  people will prefer to do things manually; eg have the minimum
                  fuel volume set to zero and handle it in the fuel map, or use
                  a minimum effective pulsewidth instead.  
  

![10_table](../images/040_Injector_SelectionInSW/10_table.png)
  
  
I’ve said it in other videos but I need to say a big
                  thank you to Paul Yaw from Injector Dynamics for his help with
                  teaching me how to characterise injectors accurately and in an
                  automated way. Without that I’d probably still be “pissing in
                  a bucket” in his words. And thank you to all who have lent or
                  sent injectors for me to measure – too many to mention but
                  they are all credited in the software.  
  
Thank you.  
  
  
©2018
        Adaptronic  
  
