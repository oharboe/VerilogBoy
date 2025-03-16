OpenROAD ASAP7 PDK configuration
================================

TL;DR Install Bazelisk and run command below to build and view design in the GUI, Bazelisk handles all dependencies.

Demonstrates how to set up an [bazel-orfs](https://github.com/The-OpenROAD-Project/bazel-orfs) to build the design with [OpenROAD-flow-scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts)

To build and view [Install Bazelisk](https://bazel.build/install/bazelisk) and run:

    bazel run //openroad:boy_cts /tmp/cts gui_cts

Estimated routing congestion
----------------------------

![alt text](histogramandroutingcongestion.png)

Ideas for future work
=====================

- A more realistic SRAM representation, currently instantiated as flip flops
  and a macro with mocked area.
- Initialize ROM correctly, for now stubbed out.
- Flesh out constraints.sdc with all the correct clocks and any false paths for
  asynchronous reset, input/output delay, etc.
- add IO constraints to place pins on one edge of the SRAMs and top level
- reduce area

[MegaBoom](https://github.com/The-OpenROAD-Project/megaboom) demonstrates a number of techniques to study a design and set up mock SRAMs.
