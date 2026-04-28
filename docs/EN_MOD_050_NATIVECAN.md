  
  
  
  
  
  
[DOWNLOADS](#)[STORE](#)[CONTACT US](#)  
  
  
  
  
  
  

CAN Protocol and the Adaptronic CAN System

[go back to
                support home](EN_EUGENE_MOD_HOME.md)  

![image](../images/Eugene/Eugene250.png)
  
  
  

[Using
                a Racepack IQ3 Dash](EN_MOD_049_RACEPAK_VNET.md)[ ](EN_EUGENE_ABOUT.md)

[Setting
                up the AEM CD7 Dash  

              ](EN_MOD_051_AEMDASH.md)

  

[  

              ](EN_SelFW.md)

  

  
  
  
  
  
  
  
  
  
This article describes the CAN
                  protocol in general, and also describes the native Adaptronic
                  CAN system.  
  
Firstly, CAN is short for Control Area Network. It
                  is a multi-drop broadcast protocol. The physical connection is
                  via a twisted pair; with a high and a low signal. When the bus
                  is in the recessive state, both high and low signals are at
                  the same voltage. When the bus is in the dominant state, the
                  high line goes to a higher voltage and the low line goes to a
                  lower voltage, with the average voltage remaining the same.
                  This provides excellent noise immunity and is a similar
                  principle to many other protocols such as RS485, RS422,
                  Ethernet and even good old analog phone lines – none of which
                  are shielded usually.  
  

![1_resistor](../images/050_NativeCAN/1_resistor.jpg)
CAN
                        Bus Diagram  

![2_Recessive](../images/050_NativeCAN/2_Recessive.png)

![3_Dominant](../images/050_NativeCAN/3_Dominant.png)
  
  
Multiple devices can be connected on the
                  bus in parallel, and there is no bus master; any device can
                  broadcast a message. The bus should be terminated at each end
                  with a 120 Ohm resistor.  
  
Because of the way CAN works, every device on the
                  bus must be set to the same bit rate. If you have two devices
                  with different bit rates on the bus, then as soon as one
                  starts to broadcast a message, the second one will see that
                  the message is corrupt (because the bitrate is wrong) and
                  actually transmit over the top to ensure that no other devices
                  can misbehave due to the corrupt message. Therefore it is very
                  important to make sure you understand the bitrates of the
                  different devices on the CAN bus.  
  
Each CAN data packet contains an identifier, which
                  is either 11 or 23 bits in length, and then up to 8 data
                  bytes. The identifier is what allows the other devices on the
                  bus to know which device sent the message and what it means.  
  
All Modular ECUs have at least one CAN bus, with
                  many such as the M6000 having a second CAN bus connection. All
                  the settings and functions are the same for both busses, so we
                  will only discuss one of them here.  
  
  
[
                  ](http://www.adaptronic.com.au/wp/wp-content/uploads/2017/08/2_terminator.jpg)
![4_2CAN](../images/050_NativeCAN/4_2CAN.png)
  
  
In the Adaptronic software there are many CAN
                  settings, and I won’t discuss them all in this article, but we
                  will discuss the basics. The first is the bitrate, as
                  discussed earlier. The default is 1 Mbps, which is also the
                  highest rate, however lower rates can also be selected so long
                  as they divide into 1 Mbps. You can also select an option here
                  to disable the CAN function completely, and that allows the
                  bus to be free (without bitrate conflicts described before).  
  

![5_Bitrate](../images/050_NativeCAN/5_Bitrate.jpg)
  
  
The second is the inbuilt termination resistor; the
                  ECU has an internal 120 Ohm resistor to terminate the CAN bus,
                  and that can be enabled or disabled using the software
                  setting. In accordance with what I described before about a
                  CAN bus needing a 120 Ohm resistor at each end of the bus,
                  this means that you should enable the termination resistor if
                  the ECU is located at one END of the CAN bus, but if it’s in
                  the middle, this should be disabled and the termination should
                  be done at each end.  
  

![6_terminator](../images/050_NativeCAN/6_terminator.jpg)
  
  
There are settings for receiving wideband over CAN,
                  and also the non-native CAN output modes such as emulation of
                  the[Racepak](file:///C:/Users/Larry%20Cruz/Dropbox/2018/Scratch/Using%20Blue%20Griffon%20to%20edit%20Eugene%20HTML%20help%20files/EN/EN_MOD_049_RACEPAK.md)or Haltech systems, but I won’t go into those here.  
  

![7_Wideband](../images/050_NativeCAN/7_Wideband.jpg)
  
  
Each CAN bus can also send out data in the
                  Adaptronic native format. This gives you a direct window into
                  the live variables inside the ECU, in the same way that
                  you can see almost any variable from within the Eugene
                  software on the gauges or monitor panels.  
  

![8_CANchannels](../images/050_NativeCAN/8_CANchannels.jpg)
  
  
All these live variables are 16 bits – so each
                  variable takes 2 bytes. Therefore, 4 of these can fit into a
                  CAN packet. The software supports up to 1024 live variables,
                  and therefore there are up to 256 different CAN packets that
                  can be sent. Each different CAN packet has a unique ID. The
                  default base address is $300, so therefore these CAN packets
                  can have the IDs in the range of $300 - $3ff. You can select
                  which channels are transmitted, so that you can avoid a whole
                  lot of data you don’t need and maximise the data rate.  
  
The settings available are as follows:  

- Bitrate, described above. The default is 1 Mbps
- Termination, the default is “on”
- Enabling of the Adaptronic CAN output
- The base address, default being $300
- Enabling of any additional CAN channels  
The channels which are always transmitted include
                  the basics like engine speed, battery voltage, manifold
                  pressure, throttle position and so on. They will appear at the
                  bottom.  
  
In addition you can send any of the
                  variables, which you can select in the software.  
  
Furthermore, you can select a function in the
                  software which generates a document showing all the variables
                  which will be transmitted.  
  
The document for the standard configuration is
                  attached.  
  
  
©2018
        Adaptronic  
  
