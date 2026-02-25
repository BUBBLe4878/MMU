# DIY Mechanical MMU (Multi‑Material Unit)

A simple, hardware‑driven MMU designed to let a 3D printer switch filaments using a mechanical selector, a stepper motor, and an external microcontroller.  
The goal is to avoid complex firmware integrations (like Klipper MMU mods) by using a physical “click‑based” signaling method between the printer and the MMU.




## 🚀 Project Overview

This MMU uses:
- A **Raspberry Pi Pico W** as the controller  
- A **stepper motor + A4988 driver** to rotate or slide a filament selector  
- **Endstop switches** for homing and for the printer to “signal” tool changes  
- Simple G‑code macros that move the print head to a click‑station to trigger filament changes  

The printer doesn’t need MMU‑aware firmware — it only performs motion patterns that the MMU interprets as commands.




## 🧠 How It Works

1. The printer reaches a fixed “MMU signal point.”
2. It performs a series of short back‑and‑forth moves.
3. An endstop detects these “clicks.”
4. The Pico counts the clicks and rotates the selector to the correct filament.
5. The printer unloads/loads filament normally.

This keeps the printer firmware simple while giving you multi‑material capability.




## 🛠️ Features

- No firmware mods required  
- Simple mechanical signaling  
- Modular design  
- Cheap, easy‑to‑source components  
- Expandable to more filaments  


