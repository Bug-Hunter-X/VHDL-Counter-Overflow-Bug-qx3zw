# VHDL Counter Overflow Bug
This repository demonstrates a common but subtle bug in VHDL code: an integer overflow in a counter.  The `buggy_counter.vhdl` file contains the buggy code.  The `fixed_counter.vhdl` file provides a corrected version.

**Bug Description:**
The original counter implementation doesn't explicitly handle potential overflow conditions. If the `count` signal reaches its maximum value (15), the subsequent increment operation might lead to unpredictable behavior or simulation errors, depending on the synthesizer or simulator used. 

**Solution:**
The solution involves explicit handling of the overflow condition using a modulo operation, ensuring that the counter wraps around correctly when it reaches its maximum value.