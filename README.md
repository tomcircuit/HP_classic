# HP_classic - LiPo Battery for HP 'Classic' Calculators
 
This is my attempt at a LiPo-based battery pack for "Classic" HP Calculators, specifically HP-35, HP-45, and HP-55.  The original NiCd packs are all dead by now, and rebuilding them is difficult - *assuming you can even find a pack to rebuild*. I thought it would be fun to use a rechargeable LiPo battery, and include the circuitry to re-charge via USB as well. 

> LiPo chemistry has very specific care-and-feeding when it comes to recharging, **you cannot use the HP AC charger to recharge this pack!**  Don't even try it.  Not kidding.

 The basic idea is to use a gold-flashed (ENIG) PCB as the contact substrate, and mount the LiPo, USB micro B receptacle, and charging circuitry on the opposite side. A pair of laser-cut 'endcaps' locate the assembly within the battery well and allow the compartment cover to hold it in place. 
 
![Mechanization](https://github.com/tomcircuit/HP_classic/blob/master/media/mechanization.png?raw=true)


## The Endcaps
I just happen to have an original NiCd HP battery pack, so I was able to measure its end profile and draw it in MS Visio and export as an SVG file. The endcap is laser-cut from 3mm thick fiberboard and its overall size is **47mm x  14mm**. I'm sure you could use some other material if you desired. I went with fiberboard in case I needed to tweak it, and because it is cheap. Two endcaps are required for each pack. 

![Laser Cut Endcap](https://github.com/tomcircuit/HP_classic/blob/master/media/endcap.png?raw=true)

I had a batch of 6 pcs made by [Ponoko](https://www.ponoko.com/) and they were very inexpensive, less than $1 each. Consider that Ponoko has a flat $14 setup charge per design, however. If you have other means to access a laser cutter, you can probably do this much more cheaply.

## The PCB 
The PCB holds the USB micro B connector, the charging circuitry, a connector for the LiPo battery, and most importantly the pads that mate with the contacts in the calculator.  The overall size of the PCB is 56mm x 40mm. The material is 1.6mm thick FR4. So that the contact pads do not  tarnish over time, I chose a gold-flash treatment (ENIG). 

The schematic and PCB were designed using KiCAD. Note that the PCB can accommodate either a JST or 0.1" two pin battery connector type.
![3D render of PCB](https://github.com/tomcircuit/HP_classic/blob/master/media/HP_classic_top.jpg?raw=true)

I had the PCB fabricated by [PCBWay](https://www.pcbway.com/)  This is the second PCB that I've had made by them, and I am once again very satisfied with the speed, quality, and price. The PCB can be ordered from them directly as a [shared project](https://www.pcbway.com/project/shareproject/HP_Classic_Calculator_LiPo_Battery_Pack.html).

## The LiPo Battery
I wanted a 1S (3.7V) LiPo battery in the neighborhood of 1000mAhr that would fit within the confines of the original pack envelope. This led me to a size "803040" LiPo battery. I prefer the JST connector, so I found one with that connector type. The PCB can accommodate either JST or "two pin" connectors, so there's some flexibility here.

I believe that a thicker battery could be used, because of the profile of the battery compartment cover. That might allow for a higher capacity battery, which would translate into longer running time. 

## Putting It All Together
Pretty self-explanatory. I used 0805 size components to allow for easy hand-soldering. Note that D1 is an LED and is polarized, so pay attention to that. Soldering the USB connector requires a fine-tip iron and some patience. 

The endcaps each need a small amount of Krazy glue to keep them in place, and the PCB edges should be flush with the outer surface of each endcap to match the overall size of the original battery pack.
> You will not be able to access the USB connector's solder joints after the endcap is installed, so be sure of your workmanship there before you glue that particular endcap in place

![Assembly showing endcap](https://github.com/tomcircuit/HP_classic/blob/master/media/showing_endcap.jpg?raw=true)

I don't know if there are 'standards' for LiPo battery connector polarity, but I managed to get a battery that had the opposite pinning than what I expected. I had to swap the polarity of the battery plug to make it match my PCB. Plug the battery in and tape it to the PCB. 

## Charge It
Connect a micro-B cable to the board and charge the LiPo battery. The LED will stay lit during the charging process, and extinguish when it is completed. The charge current is 200mA (0.2C for a 1000mAhr battery). You can adjust R1 to change the current if you need to. It took about two hours to charge my battery,

## Use It!
Install the pack into the calculator, paying attention to mate the contact pads with the contacts in the calculator. The pads are sized to prevent contact if the pack is inserted incorrectly, but I do not recommend testing to find out if I got that all right or not. My understanding is that these classic calculators will not withstand reverse voltage. Don't risk it.
![Installed Pack](https://github.com/tomcircuit/HP_classic/blob/master/media/installed.jpg?raw=true)

If you've done everything correctly, you should be greeted with 0.00 when you turn your calculator on. Your classic calculator is now sipping power from a modern, convenient, and most importantly *non-leaking* battery pack.  Enjoy!

![Happy HP45](https://github.com/tomcircuit/HP_classic/blob/master/media/success.jpg?raw=true)

November 18, 2020
Tom LeMense
rev 1
  
 
 
