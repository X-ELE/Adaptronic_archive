  
  
  
  
  
  
  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  
  
  
  
  
  

Different Ways of Handling Changes in
              Temperature on Modular ECUs

[go back to
                support home](EN_EUGENE_MOD_HOME.md)  

![image](../images/Eugene/Eugene250.png)
  
  
  

[Engine
                Protection Functions](EN_MOD_014_ENGINEPROTECTION.md)[ ](EN_EUGENE_ABOUT.md)

[Thermofan
                Control  

              ](EN_MOD_023_THERMOFAN.md)

  

[  

              ](EN_SelFW.md)

  

  
  
  
  
  
  
  
  
  
  
Like it or not, engines need to
                  operate over a range of temperatures, both ambient and the
                  temperature of the engine itself. The engine has to be above
                  the ambient temperature because it generates heat, and the
                  only way to get rid of the heat is to have it above the
                  ambient temperature. The higher the temperature, the faster
                  the heat rejection by Newton’s Law of Cooling, so most engines
                  are designed from the factory to run a bit under the boiling
                  point of water.  
  
However we want the air temperature going into the
                  engine to be as cold as possible to maximise its density,
                  subject to other considerations such as fuel condensing out of
                  suspension and so on.  
  
Fuel can also change in temperature, although that’s
                  discussed in the injector model video, not in this one.  
  
Because of all these factors, what ECUs have
                  traditionally done is to have a set of coolant temperature
                  based fuel trims and air temperature based fuel trims. Often
                  these tend to interact and produce unexpected results. So this
                  article describes the different ways in which the Modular ECU
                  can handle changes in temperature.  
  
The first way is our preferred method which is
                  called Charge Temperature Estimation. This is selected in the
                  main tuning modes page. Rather than having separate
                  corrections for air temperature and coolant temperature, the
                  ECU estimates the charge temperature and uses this single
                  variable instead to calculate the air density.  
  
The charge temperature is estimated using the heat
                  soak percentage map, which can be found under fuel tuning
                  -> temperature corrections.  
  

![1_heatsoak](../images/033_AirandCoolantCompensationsforFuel/1_heatsoak.png)
  
  
This percentage relates to how severe the heat soak
                  effect is. Normally the intake manifold will heat up to the
                  engine’s operating temperature, so the temperature of the air
                  going into the engine will be some where in between the
                  temperature of the incoming air and the coolant temperature. A
                  value of 100% in this map means that the ECU only looks at the
                  coolant temperature – so this would be an extreme case where
                  the temperature of the incoming air, measured by the air
                  temperature sensor, is irrelevant because the heat soak effect
                  is so strong that the air is at engine temperature when it
                  goes into the cylinder. A value of 0% would mean that there’s
                  no heatsoak at all, and that the air temperature sensor gives
                  you the actual temperature of the air going into the cylinder.
                  The closest case to this I can think of would be a naturally
                  aspirated, individual throttle engine with an extremely short
                  inlet tract and no plenum, but even that would have some heat
                  soak effect.  
  
In practice the heat soak effect is greater at low
                  engine speeds, and at low manifold pressures. So at idle it
                  might be as high as 70%, but at higher engine speeds on boost
                  it might be as low as 20%. These are the starting points that
                  I use and then adjust them manually if I notice a temperature
                  compensation problem.  
  
If the mixture gets richer as the air temperature
                  increases but coolant temperature remains the same, that means
                  that the heat soak value is too low and the ECU needs to
                  weight the value from the air temperature sensor more heavily.
                  If the mixture gets leaner as the air temperature increases
                  but coolant temperature remains the same, then that means the
                  ECU is giving too much weight to the air temperature sensor
                  and the heat soak percentage should be reduced.  
  
Because the charge temperature is used as part of
                  the air mass calculation, there should be no need for any
                  additional correction, and therefore the charge temperature
                  fuel trim table should be left at zero. However if you do want
                  to many any changes manually, this is where it is done. You
                  can trim the value differently at different loads as well if
                  you only want to make the difference on vacuum or on boost.  
  
If you want to do the temperature trims manually
                  instead, then you can disable the manifold heat soak system in
                  the tuning modes setup page.  
  

![2_Tempmode](../images/033_AirandCoolantCompensationsforFuel/2_Tempmode.png)
  
  
Then the ECU will use the air temperature as the
                  variable in the air mass calculation, and any trims that you
                  want to apply on top of this must be placed in the separate
                  air temp and coolant temp trim tables.  
  
Setting up engines so they behave correctly over a
                  wide range of temperatures can be fiddly if you have to do it
                  all manually, but we find that with the charge temperature
                  model, the theory actually gets the fuel calculation pretty
                  close and very little adjustment is required on top of this.  
  
Thank you very much!  
  
  
©2018
        Adaptronic  
  
