# VHDL Counter Bug: Incorrect Assignment on Max Value

This repository demonstrates a subtle bug in a VHDL counter implementation and its correction.

## Bug Description
The `buggy_counter.vhd` file contains a VHDL counter that increments from 0 to 15. However, there's an error in how it handles the counter's maximum value (15).  When `count` reaches 15, the assignment statement within the `if` condition is syntactically correct but leads to unintended behavior.

## Bug Solution
The corrected code is present in `fixed_counter.vhd`. The solution simply fixes the typo in the original assignment statement. The corrected statement should be: `count <= 0;`

## How to Reproduce
1.  Simulate `buggy_counter.vhd` using your preferred VHDL simulator (e.g., ModelSim, GHDL, etc.). Observe the incorrect counter behavior.
2. Simulate `fixed_counter.vhd` to see the corrected behavior.

## Learning Points
This example highlights the importance of carefully reviewing even the simplest of statements, especially in the context of control flow.  Small typos in VHDL code can lead to unexpected behavior and are often difficult to detect.