# XBAND Development System

- There are two development systems available:
   - System 7: Compiles XBAND-OS and assembles Madden 95, MK, MK2, NHL95 and RR3 patches
   - DOS: Assembles MK2, NBA Jam, SSF2 and generic shell patches
   
- Resolution and magnification can be set in *"BasiliskII_prefs"* and *"dosbox-x.conf"*

## Compile XBAND-OS

To compile XBAND-OS you need to build the ROMDB and the ROM in two separate steps.

1. Navigate to Sega1.0 Folder and double-click *"SEGA.ROMDB.π"* to open the project in Think C. Select **"Project/Run"** from the menu to compile and run the ROMDB application. When console outputs "SegaSound: initialized!" select **"File/Save ROM Image ..."** and save the ROM resource to the the predefined name of *"SEGA.ROM.π.rsrc"*. Overwrite existing file and finally close the console with **"File/Quit"**.

2. Double-click *"SEGA.ROM.π"* and select **"Project/Build Application"** to compile the ROM. Save the application to the predefined name of *"FuckerROM"* :grin: (with leaving "Smart Link" enabled).

3. Double-click *"π.ROMBuilder"* in the *"BuildROM"* subfolder. Execute via **"Project/Run"** again and exit the console with a press of the return-key. The generated ROM can be found as *"ROM Image"* in the same folder.

   <img src="https://user-images.githubusercontent.com/37120278/200578373-6a7806bd-c704-4fb2-8592-ac5608629d3f.png" width=50% height=50%>

## Compile XBAND-OS with FredSerial

- Copy *"FredSerial.c"* and *"FredSerialPriv.h"* to the *"Sega1.0/Comm"* Folder

- In Think C project *"SEGA.ROMDB.π"* edit the file *"FindOpponent.c"* in line 342 and comment "#define MODEM	1" out

- In Think C project *"SEGA.ROM.π"* remove *"PModem.c"* from segment 8 and add *"FredSerial.c"* instead

- Compile as described above

## Build Madden 95, MK, MK2, NHL95 and RR3 patches

- Open MPW Shell and select the patch to build in the menu

   ![image](https://user-images.githubusercontent.com/37120278/201548091-f4e272dc-9fc4-42f8-b6e8-11577ab565c3.png)

## Build MK2, NBA Jam, SSF2 and generic shell patches

- Switch to the patch directory and run the build-batchfile

   ![image](https://user-images.githubusercontent.com/37120278/201548323-138efdf0-2d66-457f-9f10-adb81ce9240e.png)
