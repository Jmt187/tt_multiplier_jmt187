<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

This project implements a 4-bit digital multiplier using Verilog.

Two 4-bit inputs, A and B, are provided through the input pins (ui_in). The design multiplies A and B using combinational logic, producing an 8-bit product P.

The input mapping is:
- ui_in[7:4] → A[3:0]
- ui_in[3:0] → B[3:0]

The output mapping is:
- uo_out[7:0] → P[7:0]

The multiplier is implemented in the module `mult.v`, and connected to the Tiny Tapeout wrapper `tt_um_mult_top.v`.

## How to test

To test the design, different values of A and B can be applied to the input pins.

For example:
- A = 3 (0011), B = 2 (0010) → Output P = 6 (00000110)
- A = 15 (1111), B = 15 (1111) → Output P = 225 (11100001)

In simulation (ModelSim), the testbench `mult_tb.v` runs 1000 random tests and verifies that the output matches the expected multiplication result.


## External hardware

No external hardware is required for this design.

The multiplier is purely digital and operates entirely within the chip.
