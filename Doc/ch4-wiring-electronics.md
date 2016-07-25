# Wiring Electronics

##Prepare the RAMPS electronics

<img width="640" class="img-responsive" src="https://farm8.staticflickr.com/7558/15472993093_a89c6e4340_o.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

###Install Jumpers

Short the PINS (Highlighted in Green) under Step Stick using Jumpers. Theses jumper determines the stepping mode of the step stick. Default is 1/16 micro stepping all 3 jumpers need to be installed under drivers for 1/16 micro stepping mode

<img width="640" class="img-responsive" src="https://farm8.staticflickr.com/7456/12460541693_46700bc0ab_n.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">
<br />
<img width="640" class="img-responsive" src="https://farm8.staticflickr.com/7380/12460528073_044c3e98f6_n.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">
    

###Installing StepStick

Install heat sink on Step Stick

<img width="640" class="img-responsive" src="https://farm9.staticflickr.com/8609/15472993203_6fc77c661b_o.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

###Assembling RAMPS and Arduino

Assembling RAMPS means simply stacking RAMPS1.4 shield on top of Mega 2560.

<img width="640" class="img-responsive" src="https://farm8.staticflickr.com/7492/15905232118_2d4d34b18c_o.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

###Note: Make sure to Match the PIN in Step Stick and RAMPS, else the step stick will be damaged

<img width="350" class="img-responsive" src="https://farm6.staticflickr.com/5531/12460525043_a5de50a480_z.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">
<br />
<img width="350" class="img-responsive" src="https://farm3.staticflickr.com/2828/12460522983_8ec4a05899_z.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">
<br />

Step Stick Assembly, note the direction of Trim Pots

<img width="350" class="img-responsive" src="https://farm3.staticflickr.com/2876/12460348065_2a39ac479d_n.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

Make sure your assembled electronics looks like the picture

<img width="640" class="img-responsive" src="https://farm3.staticflickr.com/2830/12460534493_a53b3121d2_z.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3">

###RAMPS After Assembly

<img width="640" class="img-responsive" src="https://farm9.staticflickr.com/8572/16090748001_3a308ab9d5_o.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

##Wiring Components

###Connecting Hotend, HeatBed

Connector Pairs D8, D9, D10 are used for connecting these devices.
This configuration is based on Firmware configuration (Marlin). Depending on your Marlin firmware configuration you can wire the hardware

Configuration 1: Hotend (D10) + Fan (D9) + Heat Bed (D8)
Configuration 2: Hotend (D10) + Hotend (D9) + Heat Bed (D8)

<img width="640" class="img-responsive" src="https://farm6.staticflickr.com/5498/12460366365_3b87e330c0_o.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">
<br />
<img width="640" class="img-responsive" src="https://farm6.staticflickr.com/5505/12460533303_a4aab06ba7_o.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">



###Configuration 1: Hotend (D10) + Fan (D9) + Heat Bed (D8)

Fan is optional, you can leave it unconnected

<img width="640" class="img-responsive" src="https://c2.staticflickr.com/4/3685/13183862485_c99b8d4577_b.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

###Configuration 2: Hotend (D10) + Hotend (D9) + Heat Bed (D8)

Some of India makers asked us how to connect two extruder setup

<img width="640" class="img-responsive" src="https://c1.staticflickr.com/3/2538/13183862055_791ea0e5c0_b.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">


###Connecting Thermistor, Limit switch and Power supply

Each is explained in separate sections below     

<img width="640" class="img-responsive" src="https://www.diy-india.com/static/images/prusai3/RAMPS_0.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

###Connecting End Stops

Each is explained in separate sections below    
  
<img width="640" class="img-responsive" src="https://www.diy-india.com/static/images/prusai3/RAMPS_1.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">
<img width="640" class="img-responsive" src="https://c2.staticflickr.com/8/7234/13183863015_61e35b37e0_b.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">


###Wire the power supply

<p>We have modified the power supply and pre crimped the wire, so you can just plug and play without worries.</p>
<p>We have used the branded ATX power supply, which is used in computer CPU box. The power supply has ratting of 450W-300W and can deliver up to 12V @ 15A which is sufficient for driving the PCB Heatbed and all its electronics</p>

<img width="640" class="img-responsive" src="https://www.diy-india.com/static/images/prusai3/RAMPS_2.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

###Connecting Thermistor

<img width="640" class="img-responsive" src="https://www.diy-india.com/static/images/prusai3/RAMPS_3.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">       
<p>In the Picture T0, T1, T2 are for thermistor: Hotend 1 (T0), Heat bed (T1), Hotend (T2)</p>
<img width="640" class="img-responsive" src="https://c2.staticflickr.com/8/7070/13183859175_9991e59a6d_b.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

##Connection Diagram

After following all above steps, your wiring should look like below diagrams

###Connection Diagram 1

<img width="640" class="img-responsive" src="https://farm8.staticflickr.com/7582/15470352354_3baf2e7bba_o.jpg" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

###Connection Diagram 2

<img width="640" class="img-responsive" src="https://farm8.staticflickr.com/7573/15685742014_772d025008_o.png" alt="Wiring RAMPS Electronics for RepRap Prusa i3 3D Printer">

