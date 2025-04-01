# Evaluation Metrics 

The goal of a CPU’s design is to balance **functionality**, **performance**, **power/energy**, and **cost** requirements. To quantify and compare designs, computer architects rely on **evaluation metrics** that measure speed, efficiency, and power consumption.  

This page explores some of the most common metrics and formulas used to evaluate CPU performance.

---

## Performance Evaluation

Historically, processor performance from the 1970s to the mid-2000s was driven largely by **increasing clock frequency**. Clock speeds rose steadily, and deeper pipelines allowed instructions to be processed at higher frequencies. However, power constraints eventually stalled frequency scaling. Modern CPUs rely on **parallelism**, **pipelining**, and **microarchitecture optimizations** rather than just faster clocks.

### CPU Execution Time

A classic formula for CPU execution time is:

$$
T_{\text{CPU}} = \text{Instruction Count} \times \text{CPI} \times \frac{1}{f_{\text{clock}}}
$$

where:
- **Instruction Count (IC)** is the total number of instructions executed by the program.
- **CPI (Cycles Per Instruction)** is the average number of clock cycles each instruction takes.
- $ f_{\text{clock}} $ is the clock frequency (cycles per second).

Alternatively, we often write:

$$
T_{\text{CPU}} = \text{Instruction Count} \times \text{CPI} \times t_{\text{clk}}
$$

where $ t_{\text{clk}} = \frac{1}{f_{\text{clock}}} $ is the clock period.

### Speedup

To compare a new design (or optimization) against an old baseline, we use **speedup**:

$$
\text{Speedup} = \frac{T_{\text{old}}}{T_{\text{new}}}
$$

A speedup of 2 means the new design is twice as fast (i.e., half the execution time).

### Amdahl’s Law (Brief Mention)

When an optimization speeds up only a fraction of a program, **Amdahl’s Law** helps quantify overall speedup:

$$
S = \frac{1}{(1 - p) + \frac{p}{s}}
$$

- $ p $ = fraction of execution time that can be improved.
- $ s $ = speedup of the improved portion.

Amdahl’s Law reminds us that diminishing returns set in if only part of the workload is accelerated.

---

## Power and Energy Metrics

As clock frequencies rose, **power consumption** became a critical design concern. Power roughly follows:

$$
P \approx C \cdot V^2 \cdot f
$$

where:
- $ C $ = effective switching capacitance,
- $ V $ = supply voltage,
- $ f $ = clock frequency.

Because **energy** is power over time, we have:

$$
E = P \times T_{\text{CPU}}
$$

- Reducing $ f $ (frequency) or $ V $ (voltage) can save power but may impact performance.
- Modern designs also rely on **dynamic voltage and frequency scaling (DVFS)**, **power gating**, and **multi-core** parallelism to optimize performance per watt.

---

## Balancing the Metrics

- **Performance**: Minimizing execution time (through higher IPC, parallelism, better microarchitecture).  
- **Power/Energy**: Staying within thermal budgets and maximizing battery life in mobile devices.  
- **Cost**: Factoring in manufacturing complexity, chip area, and market demands.

Ultimately, a CPU design aims to **maximize performance** under **power and cost constraints**. Since frequency alone can no longer carry performance gains, architects increasingly rely on **multi-core**, **out-of-order execution**, **speculation**, and **other parallelism techniques** to improve throughput while managing power.

---
