# CPU and Cache System using Logisim

---

## Overview

A complete CPU and Cache memory system designed and built using Logisim. The system includes key CPU components such as a Program Counter, Instruction Decoder, and Register File, alongside an 8-entry direct-mapped Cache with HIT and MISS handling logic.

---

## Learning Objectives

Through this project, I'm developing a deep understanding of:

- **CPU Architecture:** Designing a basic CPU with program counting, instruction decoding, and register handling.
- **Cache Memory Systems:** Implementing direct-mapped caching mechanisms, including HIT/MISS logic, TAG management, and Dirty/Valid bit handling.
- **Combinational and Sequential Logic:** Building circuits using fundamental gates, flip-flops, multiplexers, arithmetic, and memory components.
- **Digital Circuit Simulation:** Practicing design and debugging skills within the Logisim digital circuit simulator.

---

## Project Components

### CPU Components:
- **Program Counter (PC):** Tracks the current instruction address.
- **Instruction Decoder:** Decodes instructions to generate control signals.
- **Register File:** Stores and manages register values for operations.

### Cache System:
- **8-entry Direct Mapped Cache**
  - **Valid Bit:** Indicates if data is loaded in the cache line.
  - **Dirty Bit:** Marks whether cache data has been modified.
  - **TAG:** Identifies cached data address.
  - **Cache Data:** Actual data stored within cache lines.

---

## Operation Details

### Cache Logic:
- **Read Operation:**
  - Splits address into TAG and Entry.
  - Compares TAGs; returns cache data on HIT, fetches from RAM on MISS, and updates cache.
- **Write Operation:**
  - Splits address, checks for cache HIT.
  - Updates cache data and sets Dirty Bit on HIT; no action on MISS.

---

## Technical Specifications

### Inputs:
| Name       | Bits | Description                                        |
|------------|------|----------------------------------------------------|
| Address    | 8    | Memory address for read/write operations.          |
| CPU Data   | 8    | Data input from CPU for cache write operations.    |
| Write Data | 1    | Indicates read (`0`) or write (`1`) operation.     |
| ClkIn      | 1    | Clock input for registers/flip-flops.              |

### Outputs:
| Name      | Bits | Description                                          |
|-----------|------|------------------------------------------------------|
| Valid Bit | 1    | Indicates if cache line contains valid data.         |
| Dirty Bit | 1    | Shows if cache line data has been modified.          |
| TAG       | -    | Outputs TAGs for each Cache Line.                    |
| Data Out  | 8    | Outputs data fetched from Cache or RAM.              |

---

## Tools & Technologies

- **Simulator:** Logisim
- **Components:** Multi-Gates, Flip-Flops, Multiplexers, Arithmetic Units, RAM

---

## Future Improvements

- Implementing associative caching
- Enhancing write-back or write-through strategies (Based on LRU & MRU)
- Integrating more advanced instruction sets and decoding logic

---

## License

Licensed under the MIT License – see [LICENSE](LICENSE) file for details.

---

**[Back to top](#cpu-and-cache-system-using-logisim)**

