# Velcheck PSI Reproduction Project

**PSI** : Process State Indicator, the round color light seen on R2-D2's dome (one blue/red in front, one yellow/green in rear)

**Velcheck** : Pioneering member of the R2 Builders Club, 80's synth virtuoso

In the early days of the R2 Builders, Mike Velcheck designed and supplied a PSI for club members around the world. His design has been the basis for most PSI's since, all sharing the same footprint, many with an abundance of LEDs and fancy swipe animations, none as simple and plug-n-play friendly as Mikes. In December of 2021 Mike passed away.

This project aims to bring back Mike Velcheck's great PSI design. Using a donor unit, I reverse clumgeneered Mike's PCB, making a couple of very minor tweaks to the layout. An unused capacitor was removed, in it's place is a Devo Energy Dome. The resulting Eagle PCB and schematic files are found within, along with gerber files for production, and Mike's own instruction manual.

**Checkerboard or Side by Side?**

By moving two resistors on the board, it can be configured with LEDs in a checkerboard layout (giving a better 'spead' of each color), or side-by-side layout (which allows the PSI to appear 'stuck' with both red and blue lit at the same time).

**Using with JEDI Displays**

The PIC IC can be removed, and two wires run from a JEDI Display controller. This allows the JEDI Display to set the PSI's to their specific colors (useful during animations) rather than the onboard PIC.
