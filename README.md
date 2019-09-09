# alt_posit
Bit reverses regime bits and places them after the fraction bits to eliminate aligning the fraction during pack/unpack

FPGA oriented implementation of Gustafson's Posit floating-point numbers.
Intended for experimentation:
Optimize regime bits so fraction shifting unnecceesary on un-pack and pack of the Posit number.
  However the alt-posit format does not support using integer comparison (requires dedicated compare hardware)
Support various tapper schemes such as IEEE-754 with gradual overflow and combinations of Posit and IEEE-754 encoding.
Support unbiased "von Neumann" rounding (reduces number of fraction bits by one)
Implementation model is that of a RISC core having a register file and pipelined function units.
