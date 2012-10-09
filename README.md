Guide to Developing for the MSP430 with (Debian) Linux
======================================================

Install Packages
----------------

Make sure you are on the wheezy (testing) suite
 
* `binutis-msp430`  
Binary utilities supporting TI's MSP430 targets

* `gcc-msp430`  
GNU C compiler (cross compiler for MSP430) 

* `gdb-msp430`  
The GNU debugger for MSP430

* `msp430-libc`  
 Standard C library for TI MSP430 development

Paste this command into the terminal to install all of these packages:

    sudo apt-get install binutils-msp430 gcc-msp430 gdb-msp430 msp430-libc


Compile the Example
-------------------

To compile the example, use the makefile

    make

Or, the full syntax for the mspgcc command is:

    msp430-gcc -mmcu=msp430g2553 launchpad.c -o launchpad.elf

Converting Code Composer Programs
---------------------------------

If you are trying to compile a program written in Code Composer with GCC, you will run into trouble because they use a different syntax for interrupt service routines. Fortunately, it is fairly simple to convert it over.

**Code Composer Style Interrupts:**

    #pragma vector=TIMERA1_VECTOR
    __interrupt void ta1_isr(void)
    {
        ...
    }

**GCC Interrupts:**
    
    interrupt (TIMERA1_VECTOR) ta1_isr(void)
    {
        ...
    }






