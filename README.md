# Cinema_Light_DMX512
This is my graduate qualification work. It controls LED lighting via DMX512. And has GPIO and Ethernet interfaces and IR-remote control

12/06/2019
- Added Ethernet connection! Device can be controlled by TCP text commands from computer and etc.
The commasds are:
- 'N': On;
- 'F': Off;
- '5': 50%;
- 'L': Light;
- 'D': Dark;
- 'S':Stop;
- '1','2','3', 'A': 1, 2, 3, All zones;
- 'E': Emergency;
- '+' and '-': Up and Down;
- 'G': View settings (Send text with settings to "client");
- 'M'№ of zone'0-255': set max brightness of zone (if № = 4, brightness of all zones);
- 'R'123': set fade time of On/Off (1*10 + 2 + 3*0.1);
- 'C'123': set fade time of Light/Dark (1*10 + 2 + 3*0.1).

17/05/2019
- Changed variables' types to more appropriate (brightness and time can't be negative or too big, memory is sliiiightly freer);
- Fixed interface after exiting Settings menu (and packed some functions for interface).

11/05/2019
- Added keyboard from Ricoh FT4215 (A128) (150 ms period for debouncing, but sometimes it doesn`t help, because Start button is fubar);
- Fixed "Watch settings" to "View settings";
- Plans: make .h and .cpp files for functions and etc.

04/04/2019
- Now configuration (settings of max brightness and fade time) is saved in EEPROM (keep safe after turning off);
- Added "Watch settings" option to Settings menu. Now you can see max brightness of zones and fade time for fast and slow modes;
- Increased max fade time to 60 s, default time of slow fade is 10s and fast fade - 1s;
- Fixed interface in Setting up LIGHT/DARK and ON/OFF time.

03/04/2019
- Fixed some stuff about "fade";
- "Settings" now is "Back" button in Settings menu;
- Brightness in Settings menu is written in (0-255) range and percents (0.00%).

02/04/2019
- Added LCD-display for indication of modes, chosen zone and brightness of zones;
- Added Menu for setting maximum brightness and fading speed;
- Fixed type of delays (from int to long int). Now default fade time is 1,5 and 7 seconds;
- Fixed 50% brightness from 178 to 127 (what was i thinking about?).

26/03/2019
- Main_sketch works! Now it is DMX512 transiever controlled by IR-remote;
- Brightness is changing in Timer3 interrupts, so the mode can be chosen immediately;
- There are ON/OFF, LIGHT/DARK, 50%, STOP, EMERGENCY modes, manual brightness changing (by Up and Down);
- Each zone can be selected. 

22/03/2019
- Decided to use Mega2560, because it has more external interrupts, GPIOs, Timers and USARTs;
- Tested Arduino four universes DMX 512 library (Toni Merino (C)) and rewrited some vector names to new;
- Tested IRremote library (z3t0 (C)) on my Mega2560;
- Uploaded libraries, notes and test pieces to GitHub for convenience.
