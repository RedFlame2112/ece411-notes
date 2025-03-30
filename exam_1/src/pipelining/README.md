# Pipelining - Intro

Pipelining is a fundamental technique in CPU design that increases instruction throughput by overlapping the execution phases of multiple instructions. Instead of waiting for one instruction to fully complete before starting the next, pipelining breaks down the execution process into discrete stages (such as fetch, decode, execute, memory access, and write-back). This allows each stage to process a different instruction concurrently, resulting in improved overall performance.

Below is the structure of the pipelining section in this book. Each link provides access to detailed discussions on various aspects of pipelining.
## Table of Contents

- [Pipelining - Intro (this page)](./README.md)
    - [Pipelined Datapath](./datapath.md)
    - [Hazards](./hazards/README.md)
        - [Control Hazards](./hazards/control_hazards.md)
        - [Data Hazards](./hazards/data_hazards.md)
        - [Structural Hazards](./hazards/structural_hazards.md)
    - [Control Path](./control_unit.md)
    - [Forwarding](./forwarding.md)
    - [Stall](./stall.md)
    - [Branch Prediction](./branch_prediction.md)
    - [Instruction Parallelism](./parallelism.md)
