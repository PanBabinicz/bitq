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

![NAND-SR-LATCH-BB](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_sr_latch_bb.jpg)

#### NAND SR Latch Clocked

*The clock is a square-wave signal. Because the clock (abbreviated CLK) drives both NAND gates, a low
CLK prevents S and R from controlling the latch. If a high S and a low R drive the gate inputs,
the latch must wait until the clock goes high before Q can be set to 1. Similarly, given a low S
and a high R, the latch must wait for a high CLK before Q can reset to 0. This is an example of positive
clocking, making a latch wait until the clock signal is high before the output can change.*

![NAND-SR-LATCH-CLK](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_sr_latch_clk.png)

### D Latch

*The RS flip-flop is susceptible to a race condition. The design can be modified to eliminate the possibility
of a race condition. The result is a new kind of flip-flop known as a D latch.*

#### NAND D Latch

![NAND-D-LATCH](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_d_latch.png)

![NAND-D-LATCH-BB](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_d_latch_bb.jpg)

#### NAND D Latch Clocked

*A low CLK disables the input gates and prevents the latch from changing states. In other
words, while CLK is low, the latch is in the inactive state and the circuit stores or remembers.
When CLK is high, D controls the output. A high D sets the latch, while a low D resets it.*

![NAND-D-LATCH-CLK](https://github.com/PanBabinicz/bitq/blob/master/doc/screenshots/nand_d_latch_clk.png)

#### NAND D Latch Edge Triggered

*The RC circuit is placed at the input of a D flip-flop. By deliberate design, the RC time
constant is much smaller than the clock's pulse width. Because of this, the capacitor can
charge fully when CLK goes high. This exponential charging produces a narrow positive voltage
spike across the resistor. Later, the trailing edge of the clock pulse results in a narrow
negative spike. The narrow positive spike enables the input gates for an instant. The narrow
negative spike does nothing. The effect is to activate the input gates during the positive spike,
equivalent to sampling the value of D for an instant. At this unique time, D and its complement
hit the flip-flop inputs, forcing & to set or reset.*

## Instruction register

*The instruction register is part of the control unit. To fetch an instruction from the memory the computer does a memory read operation.
This places the contents of the addressed memory location on the W bus. At the same time, the instruction register is set up for loading
on the next positive clock edge.*
