# Bitq Regs

## Flip flop

*A flip-flop is a device with two stable states; it remains in one of these states until triggered into the other.*

### SR Latch

*The circuit shown below is a basic NAND latch. The inputs are generally designated S and R for Set and Reset respectively.
Because the NAND inputs must normally be logic 1 to avoid affecting the latching action, the inputs are considered to be inverted
in this circuit (or active low).*

#### NAND SR Latch

*Because of the NAND-gate inversion, the inactive and race conditions are reversed. In other words, R = 1 and S = 1
becomes the inactive state; R = 0 and S = 0 becomes the race condition. Therefore, whenever the NAND latch is used,
it must be avoided to have both inputs low at the same time.*

![NAND-SR-LATCH](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_sr_latch.png)

#### NAND SR Latch Clocked

*The clock is a square-wave signal. Because the clock (abbreviated CLK) drives both NAND gates, a low
CLK prevents S and R from controlling the latch. If a high S and a low R drive the gate inputs,
the latch must wait until the clock goes high before Q can be set to 1. Similarly, given a low S
and a high R, the latch must wait for a high CLK before Q can reset to 0. This is an example of positive
clocking, making a latch wait until the clock signal is high before the output can change.*

![NAND-SR-LATCH-CLK](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_sr_latch_clk.png)

### D Latch

![NAND-D-LATCH](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_d_latch.png)

## Instruction register

*The instruction register is part of the control unit. To fetch an instruction from the memory the computer does a memory read operation.
This places the contents of the addressed memory location on the W bus. At the same time, the instruction register is set up for loading
on the next positive clock edge.*
