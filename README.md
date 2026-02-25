# Mechanical MMU for ender 3

THis is a hardware‑driven MMU designed to let my 3D printer switch filaments using simple parts, a stepper motor, and an external microcontroller.  
The goal is to avoid complex firmware stuff (like Klipper) by using an endstop to signal the MMU to change.




##  Project Overview

This MMU uses:
- A Raspberry Pi Pico W
- A stepper motor + A4988 driver
- Endstop switches  
- G‑code for on filament changes  

It only performs motions(on the endstop) and the MMU will interpret it as commands.




##  How It Works

1. The printer runs into the endstop to signal color change.
2. An endstop detects the printer running into it.
3. The Pico counts the clicks and rotates the selector to the correct filament. (I will only do this if this becomes popular if not, then just 2 colors).
4. The printer unloads/loads filament normally.

This will keep the printer firmware simple while giving multi colors.




##  Features

1.No firmware mods  
2.Mechanical signaling  
3.Modular design(LATER) 
4.CHEAP, especially if you have thease components on hand.  


