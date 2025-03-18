 Decoder (2-to-4 and 3-to-8) - Theory, Design & Implementation**

### Concept Overview
A **Decoder** is a combinational circuit that converts binary-coded inputs into a unique output pattern. Decoders are widely used in memory addressing, data demultiplexing, and display systems.

### Detailed Explanation

#### ✅ 2-to-4 Decoder
- **Definition:** A 2-to-4 decoder has 2 input lines (`A`, `B`) and 4 output lines (`Y0` to `Y3`). Each output is activated based on the binary input combination.
- **Boolean Expressions:**
  - `Y0 = ~A • ~B`
  - `Y1 = ~A • B`
  - `Y2 = A • ~B`
  - `Y3 = A • B`
- **Truth Table:**

| A | B | Y0 | Y1 | Y2 | Y3 |
|:-:|:-:|:--:|:--:|:--:|:--:|
| 0 | 0 |  1 |  0 |  0 |  0 |
| 0 | 1 |  0 |  1 |  0 |  0 |
| 1 | 0 |  0 |  0 |  1 |  0 |
| 1 | 1 |  0 |  0 |  0 |  1 |

**Example Application:** Used in memory selection, address decoding, and multiplexing systems.

#### ✅ 3-to-8 Decoder
- **Definition:** A 3-to-8 decoder has 3 input lines (`A`, `B`, `C`) and 8 output lines (`Y0` to `Y7`). Each output corresponds to one of the eight possible input combinations.
- **Boolean Expressions:**
  - `Y0 = ~A • ~B • ~C`
  - `Y1 = ~A • ~B • C`
  - `Y2 = ~A • B • ~C`
  - `Y3 = ~A • B • C`
  - `Y4 = A • ~B • ~C`
  - `Y5 = A • ~B • C`
  - `Y6 = A • B • ~C`
  - `Y7 = A • B • C`

- **Truth Table:**

| A | B | C | Y0 | Y1 | Y2 | Y3 | Y4 | Y5 | Y6 | Y7 |
|:-:|:-:|:-:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| 0 | 0 | 0 |  1 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |
| 0 | 0 | 1 |  0 |  1 |  0 |  0 |  0 |  0 |  0 |  0 |
| 1 | 1 | 1 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  1 |

**Example Application:** Used in binary-to-decimal conversion, memory decoding, and logic control.


### Code Explanation
- **`assign` Statements:** Implements each output's logic based on the input combination.
- **`$monitor` Task:** Displays real-time changes in inputs and corresponding outputs.
- **Test Cases:** Ensures the expected output for various combinations of inputs.

### Execution Steps
1. Copy the Verilog code into your simulator (e.g., ModelSim, Xilinx Vivado, etc.).
2. Compile and run the code.
3. Verify that the outputs match the expected truth table values.

### Real-World Example for Practice
- Design a **4-to-16 Decoder** using two 3-to-8 decoders with an additional control line.


