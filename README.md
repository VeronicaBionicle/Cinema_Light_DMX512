# Cinema_Light_DMX512
This is my graduate qualification work. It controls LED lighting via DMX512. And has GPIO and Ethernet interfaces and IR-remote control

02/04/2019
- Added LCD-display for indication of modes, chosen zone and brightness of zones.
- Fixed type of delays (from int to long int). Now fade time is 1,5 and 7 seconds.

26/03/2019
- Main_sketch works! Now it`s DMX512 transiever controlled by IR-remote.
- Brightness is changing in Timer3 interrupts, so the mode can be chosen immediately.
- There are ON/OFF, LIGHT/DARK, 50%, STOP, EMERGENCY modes, manual brightness changing (by Up and Down).
- Each zone can be selected. 

22/03/2019
- Decided to use Mega2560, because it has more external interrupts, GPIOs, Timers and USARTs;
- Tested Arduino four universes DMX 512 library (Toni Merino (C)) and rewrited some vector names to new;
- Tested IRremote library (z3t0 (C)) on my Mega2560;
- Uploaded libraries, notes and test pieces to GitHub for convenience.
