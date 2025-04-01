# Hazards - Overview

Hazards in a pipelined processor are conditions that prevent the next instruction in the instruction stream from executing in the following cycle. These arise when the flow of instructions through the pipeline encounters conflicts or dependencies that cannot be resolved in a single cycle. There are three main categories of hazards:

1. **Data Hazards**  
   - Occur when instructions depend on the results of previous instructions that have not yet completed.  
   - **Example**: An `ADD` instruction writes its result in the Write-Back stage, but a subsequent `SUB` instruction needs that result in the Execute stage.  
   - **Resolution**: Forwarding (bypassing) can often supply the needed result directly from a later stage (EX or MEM) to an earlier stage (EX). In cases like a load-use hazard, where the data is only available after the memory access, a stall (pipeline bubble) may be necessary.

2. **Control Hazards**  
   - Arise from instructions that change the flow of execution (branches, jumps).  
   - **Example**: The pipeline fetches instructions sequentially, but a taken branch redirects the PC, invalidating the instructions that were already fetched.  
   - **Resolution**: Use branch prediction (static or dynamic) to guess the next PC. If the guess is wrong (branch misprediction), the pipeline flushes the incorrect instructions. More advanced predictors reduce misprediction penalties.

3. **Structural Hazards**  
   - Happen when two or more instructions require the same hardware resource at the same time.  
   - **Example**: A unified memory for both instructions and data could lead to conflicts if the pipeline attempts to fetch an instruction and read/write data in the same cycle.  
   - **Resolution**: Provide duplicate resources (e.g., separate instruction and data memories) or carefully schedule instructions to avoid conflicts.

---

**Key Points**  
- **Forwarding** and **stalling** address **data hazards**.  
- **Branch prediction**, **flushing**, and careful pipeline design handle **control hazards**.  
- **Resource duplication** or scheduling can mitigate **structural hazards**.  

Hazards are an inherent aspect of pipelining. Understanding and mitigating them is critical for achieving high throughput and low CPI in a pipelined CPU design.
