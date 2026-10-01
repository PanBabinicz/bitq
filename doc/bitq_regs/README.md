# Bitq Regs

## SR Latch

*The circuit shown below is a basic NAND latch. The inputs are generally designated S and R for Set and Reset respectively.
Because the NAND inputs must normally be logic 1 to avoid affecting the latching action, the inputs are considered to be inverted
in this circuit (or active low).*

### NAND SR Latch

![NAND-SR-LATCH](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_sr_latch.png)

## Instruction register

*The instruction register is part of the control unit. To fetch an instruction from the memory the computer does a memory read operation.
This places the contents of the addressed memory location on the W bus. At the same time, the instruction register is set up for loading
on the next positive clock edge.*