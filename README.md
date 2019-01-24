# MOJO-ALUGAME
For MOJO V3 FPGA. a simple or/nor/and game where selecting a tile operates on that tile and that of the other tiles beside it.<br>
Takes place on a 4 by 4 board.<br>
The objective of the game is to light up all pieces of the board. <br>
A simple project to program a game 8bit adder using the MOJO FPGA, written in Lucid.<br>
Built based off my other repository named ALU8bit
## Starting up (Prerequisites)
Preferably Utilise:<br>
Mojo IDE: https://alchitry.com/pages/mojo-ide <br>
Xillinx's ISE Design Suite for Windows 10 - 14.7  - https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/design-tools.html <br>
### Tools
Embedded Micro MOJO V3 - https://alchitry.com/collections/all/products/mojo-v3 <br>
Embedded Micro IO Shield - https://alchitry.com/collections/all/products/io-shield <br>
### Format
* adder.luc -> Does addition using bits provided.<br>
* alumod.luc -> Controls which operation occurs.<br>
* bitshift.luc -> aids in choosing which bitshift module will be used. Coordinates the next 3 modules.<br>
* bitshiftleft.luc -> Bitshift Left<br>
* bitshiftright.luc -> Bitshift Right<br>
* bitshiftrightwithsign.luc -> Bitshift right with sign<br>
* boolean.luc -> Performs a boolean operation on the 2 sets of 8 bits provided, and displays the result in the third LED array.<br>
* comparator.luc -> Utilised in the bitshift right with sign, to tell if we should light up the <br>
* io_shield.ucf -> Config file for IO_shield. leave well alone.<br>
* mojo_top.luc -> Overall controller. Really just acts as a pointer into alumod.luc<br>
* multiplier.luc -> Performs multiplication.<br>
* totaladder.luc -> Spawns 8 copies of adder.luc, for all 8 bits.<br>
* countertype.luc -> essentially a timer by incrementing a number based off the inbuilt clock of the MOJO V3 to obtain time passed in seconds.
* discerninput.luc -> based off the original mode that was selected by a user, return a different result. Used to signify to other modules which bits are to be operated on.
* impactlogic.luc -> used to hold all the different states in which the machine operates in. The pivotal component for this game to work.
* lookintoy.luc -> used to select bits.
