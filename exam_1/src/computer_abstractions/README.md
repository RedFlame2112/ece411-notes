# Computer Design – Intro

Computer design (also often referred to as *computer architecture*) is about understanding how hardware and software interact at various levels to create a functioning system. It covers everything from high-level functional specifications (the **ISA**, or Instruction Set Architecture) down to transistor-level circuits.

**In this chapter, we will:**
- Discuss the role of the **ISA** in defining how software commands translate into hardware operations.
- Explore **Moore’s Law** and how it shapes technology trends and design constraints.
- Introduce **Evaluation Metrics** such as performance, power consumption, and cost.
- Provide a high-level look at **Basic Microarchitectures**, which implement the ISA efficiently.

---

### Why Study Computer Design?

1. **Performance vs. Cost Trade-offs**  
   - Understanding how to balance speed, power usage, and manufacturing cost is central to computer design.  
   - Designers must make choices about instruction complexity, parallelism, caching, etc.

2. **Historical Context and Trends**  
   - Moore’s Law suggests transistor counts double every 18–24 months, but physical and economic constraints are increasingly challenging.  
   - New paradigms like multicore processors, GPUs, and domain-specific accelerators (e.g., AI chips) illustrate the ongoing evolution.

3. **Layers of Abstraction**  
   - The ISA is the interface between hardware and software.  
   - Microarchitecture is the “blueprint” of how instructions are actually executed under the hood.  
   - Circuit design implements the microarchitecture using logic gates and transistors.

---

### References to Other Sections

- For an overview of design, see: [Architectures/ISA](./architectures.md)  
- For trends in the computing space, see: [Moore’s Law](./moores_law.md)  
- For evaluation of microarchitectures, see: [Evaluation Metrics](./evaluation_metrics.md)  
- For an intro to microarch design, see: [Basic Microarchitectures](./microarchitectures.md)

---

You can expand on these bullet points with figures, historical notes, or real-world examples (e.g., referencing popular CPU families or architectures) to help give context. This introductory section should give a big-picture understanding of **why** the subsequent topics matter and **how** they fit together in the broader study of computer organization and design.
