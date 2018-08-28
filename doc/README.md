Note that I am using Ubuntu 16.04 LTS and gcc/make from a command line.

Tools:

To build this port, you will need an ARM cross compiler:
Download and install from the following location:

https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads


Note if you are already building the TI starterware you should have the ARM 
 cross-compiler installed and the LIB_PATH set.


To build:

Set LIB_PATH environment variable to point to the ARM tool chain.

For example:

export LIB_PATH=/home/myname/arm_tools/gcc-arm-none-eabi-4_7-2012q4

Modify the Makefile. The end of line 28 needs to match the version of the ARM 
 cross-compile that you are using or downloaded. You can check the version by
 doing the following:

cd $LIB_PATH/lib/gcc/arm-none-eabi
ls

The ls command should display a directory name that is a version number. Use
 this for the end of line 28.

In the top level directory do the following:

make clean
make

If the build is successful, there should be an app file in the bin_files
 directory.

Create a MICRO SD card.

Use the procedure at this link to create a bootable SD card

http://processors.wiki.ti.com/index.php/SD/MMC_format_for_OMAP3_boot

Copy the mlo and app file located in the bin_files directory to the SD card.

Put the SD card in the pocketbeagle.

Connect a USB to serial adapter such as a FTDI FT2232 to the pocketbeagle.
 The wiring should be:

    Pocketbeagle         FTDI board
     P1 - 30 (TX)          RXD
     P1 - 32 (RX)          TXD 
     P1 - 20 (GND)         GND

Start a serial terminal session. On Ubuntu you can use Putty with the
 following values:

BAUD - 115200
Data - 8
Stop - 1
Parity - None
Flow cntl - None 


Power on the pocketbeagle


You should see the following on the terminal screen. If you see a series of "C" being printed, then the SD card is not correct.

To keep the sample output below short, a number of lines were replaced by
****   more stack data ********

StarterWare AM335x Boot Loader

SD Card version : 2, High Capacity

1 Set Bus width

2 Set Bus speed

Copying application image from MMC/SD card to RAM

Jumping to StarterWare Application...

Platform initialized.
Initialising stack of task!

80008cb4 : 0
80008cb8 : 0

****   more stack data ********

80008d30 : 800001f0
80008d34 : 1f

Task 800001f0 succesfully created.

Initialising stack of task!

80009cb4 : 0
80009cb8 : 0

****   more stack data ********

80009d30 : 80000274
80009d34 : 1f

Task 80000274 succesfully created.

Initialising stack of task!

80009f14 : 0
80009f18 : 0

****   more stack data ********

80009f90 : 8000308c
80009f94 : 1f

Enabling timer interrupt!

Dumping context before restoring context

******  Dump of stack ****************


Task 2 message 0!
Task 1 message 0!
Hello from idle task
Task 2 message 1!
Task 2 message 2!
Task 1 message 1!
Task 2 message 3!
Task 2 message 4!

**** etc *****************
