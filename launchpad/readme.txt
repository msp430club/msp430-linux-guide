MSP-EXP430G2 LaunchPad User Experience gcc project readme
1. File listing:
 - launchpad.c: main application code
 - makefile: makefile customized for the project
2. Compiler requirements
 - msp430gcc compiler should be installed
 - msp430gcc header files should be installed with their include path added to the OS environment.
3. Using provided makefile:
 - Build with: make 
 - Clean with: make clean
 - Packge & Distribution with: make dist
4. Debug with:
 - mspdebug rf2500 [The emulator & usb drivers for the LaunchPad are similar to the ones for the ez430-rf2500]
 - Use mspdebug to start a gdbproxy & use msp430-gdb to connect & debug
