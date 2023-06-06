# double_dabble_BIN2BCD
# Binary to BCD Converter

The `bin2bcd` module is a Verilog code that converts a binary number to Binary-Coded Decimal (BCD)
format and provides the BCD digits as output. It also allows the output to be transmitted via UART in ASCII code.

## Usage

The `bin2bcd` module takes the following inputs:

- `enb`: Enable signal to indicate when the conversion should be performed.
- `clk`: Clock signal for synchronization.
- `reset_n`: Active-low reset signal to initialize the module.
- `bin`: Input binary number to be converted to BCD.

The module provides the following outputs:

- `bcd`: Output wire representing the BCD representation of the input binary number.
- `s0-s6`: Output wires representing the BCD digits in 8-bit ASCII code for UART transmission.

## Implementation Details

The conversion from binary to BCD is performed using a combination of sequential and combinational logic.
The sequential logic is triggered by the clock and reset signals, while the combinational logic performs the actual conversion.

The conversion process involves breaking down the binary number into individual BCD digits.
Each 4-bit BCD digit is then converted to its corresponding ASCII code for UART transmission.
