# Velcheck PSI Reproduction Project

**PSI** : Process State Indicator, the round color light seen on R2-D2's dome (one blue/red in front, one yellow/green in rear)

**Velcheck** : Pioneering member of the R2 Builders Club, 80's synth virtuoso

In the early days of the R2 Builders, Mike Velcheck designed and supplied a PSI for club members around the world. His design has been the basis for most PSI's since, all sharing the same footprint, many with an abundance of LEDs and fancy swipe animations, none as simple and plug-n-play friendly as Mikes. In December of 2021 Mike passed away.

This project aims to bring back Mike Velcheck's great PSI design, so that it may continue to make its way into droids. Using a donor unit, I reverse clumgeneered Mike's PCB, making a couple of very minor tweaks to the layout. An unused capacitor was removed, in it's place is a Devo Energy Dome. The resulting Eagle PCB and schematic files are found within, along with gerber files for production, and Mike's own instruction manual.

**Usage** 

See Mike's PDF user guide in this repository.

**Through-Hole Assembly**

The boards come partially assembled, but the through-hole components will need to be soldered in place. Before starting, you should decide on your LED layout (see Checkerboard vs Side by Side beloe).

 * Being mindful of polarity and color placement, each LED can then be soldered in place.
 * Next, you'll want to solder the 8-pin IC socket, which the PIC MCU (U1) will eventually sit in.
 * Solder the jumper pins for JP1 and JP2.
 * Solder the 2-pin and 4-pin screw terminals.
 * Carefully insert the pre-programmed PIC MCU into its socket.

To test, apply 12V to the 2-pin screw terminal (being mindful of polarity). 

**Checkerboard vs Side by Side?**

By moving two resistors on the board, it can be configured with LEDs in a checkerboard layout (giving a better 'spead' of each color), or side-by-side layout (which allows the PSI to appear 'stuck' with both red and blue lit at the same time). The board uses 220 ohm ressitors to limit current to each branch of 3 LEDs. For checkerboard layout, R9 and R10 should not be populated. For side-by-side layout, R8 and R5 should not be populated.

**Using with JEDI Displays**

The PIC IC can be removed, and two wires run from a JEDI Display controller. This allows the JEDI Display to set the PSI's to their specific colors (useful during animations) rather than the onboard PIC.

**Bill Of Materials**

For LEDs, high brightness and 120 degree viewing angle is recommended. For standard R2-D2 colors, you'll need 6 red, 6 blue, 6 yellow, 6 green. In the US, SuperBrightLEDs sell suitable 5m LEDs for about 50c each. These offer better spread of color than typical cheap 5mm LEDs.

 * U1 : PIC10F202-I/P 8-bit MCU (typically in an )
 * U2 : AS78L05RTR-E1 5V LDO
 * C2 : 330nf 50V 0805 X7R capacitor
 * C3 : 100nf 50V 0805 X7R capacitor
 * R1, R2 : 10K ohm 0603 resistor
 * R3, R6 : 3.3K ohm 0603 resistor
 * R4, R5, R7, R8 : 220 ohm 0603 resistor
 * D1-D12 : 5mm LEDs, various colors
 * D13 : 1N4001 diode
 * Q1, Q2 : MBT2222A BJT NPN transistor
 * P1 : 2-pin 2.54mm pitch screw terminal
 * P2 : 4-pin 2.54mm pitch screw terminal
 * JP1 & JP2 : 2.54mm 2-row 2-column male pin header
