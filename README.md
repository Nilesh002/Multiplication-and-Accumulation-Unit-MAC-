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
\```verilog
mac32 my_mac_inst (
    .a(a_input),
    .b(b_input),
    .clk(clk),
    .rst(rst),
    .p(mac_output)
);
\```

## Simulation
Simulation of the Verilog modules can be performed using a Verilog simulator. A testbench (`mac32_tb`) is provided to verify the functionality of the MAC module.

To simulate:
1. Compile the Verilog source files along with the testbench.
2. Run the simulation using your preferred Verilog simulator.

### Simulation results
![Simulation Waveform](https://github.com/Nilesh002/Multiplication-and-Accumulation-Unit-MAC-/assets/105161049/9dc23196-3f59-425c-b66c-5f09dba5ddb4)

## Schematic
The MAC module synthesized schematic consists of:
- Total cells: 222
- Total nets: 1001
- Total I/O ports: 130

![Synthesized Schematic](https://github.com/Nilesh002/Multiplication-and-Accumulation-Unit-MAC-/assets/105161049/1107b4c6-aa84-4475-a11a-436463a0e34c)

## Vivado Project
This project was developed using Xilinx Vivado. The Verilog modules can be integrated into a Vivado project for further synthesis, implementation, and verification.

## Contribution
Contributions to this project are welcome! To contribute:
1. Fork the repository.
2. Make your changes.
3. Submit a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Issues
Report any issues or feature requests in the [issue tracker](https://github.com/Nilesh002/Multiplication-and-Accumulation-Unit-MAC-/issues).
