# Verilog Multiply Accumulate (MAC) Module with Vedic Multiplication

## Overview
This repository contains Verilog code for a Multiply Accumulate (MAC) module implemented using Vedic multiplication techniques to reduce the number of partial products. The MAC module performs 32-bit multiplication and accumulation. The project was developed using Xilinx Vivado.

### Vedic Multiplication
Vedic mathematics offers efficient multiplication techniques like Nikhilam Sutra (general multiplication), Urdhva-Tiryagbhyam Sutra (vertical and crosswise), and others. These techniques exploit patterns in multiplication to reduce the number of partial products and simplify the multiplication process.

## Verilog Modules
The Verilog code includes the following modules:
- `mul16`: Multiplies two 16-bit inputs using Vedic multiplication.
- `mul8`: Multiplies two 8-bit inputs using Vedic multiplication.
- `mul4`: Multiplies two 4-bit inputs using Vedic multiplication.
- `mul2`: Multiplies two 2-bit inputs using Vedic multiplication.
- Various addition modules for different bit widths.

## MAC Module
The top-level module `mac32` implements the Multiply Accumulate operation using Vedic multiplication techniques. It multiplies two 32-bit inputs (`a` and `b`) and accumulates the result in a 64-bit accumulator.

## Usage
To use the MAC module in your Verilog design:
1. Instantiate the `mac32` module.
2. Connect appropriate inputs (`a`, `b`), clock (`clk`), and reset (`rst`) signals.
3. Connect the output of the `mac32` module to the desired destination in your design.

Example instantiation:
```verilog
mac32 my_mac_inst (
    .a(a_input),
    .b(b_input),
    .clk(clk),
    .rst(rst),
    .p(mac_output)
);
