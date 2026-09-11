<div align="center">
  <img src="https://avatars.githubusercontent.com/Rivoryxa-Technologies" width="130" alt="Rivoryxa Technologies" />

  # Rivoryxa Technologies

  **RISC-V verification. Proofs, checked waivers, and directed tests, with evidence you can rerun on open tools.**

  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Rivoryxa%20Technologies-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/company/rivoryxa-technologies/)
  ![RISC-V](https://img.shields.io/badge/RISC--V-Verification-283272)
  ![Formal](https://img.shields.io/badge/Formal-SymbiYosys-6E4C13)
</div>

---

Rivoryxa Technologies is a RISC-V verification company. Send us the bug report or the coverage hole. We return a proof, a checked waiver, or a test that reaches it, at a defined scope, with evidence you can rerun on open tools.

We specialize in RISC-V verification, formal verification, RTL debugging, coverage analysis, compliance testing, and verification automation.

Every engagement is a list of specific questions about a specific piece of RTL. For each one we investigate, produce evidence, and hand back a result you can reproduce without us and without a tool licence. Problem, investigation, evidence, reproducible result. That is the whole method.

We work on open source tools (Verilator, SymbiYosys, Yosys, z3, cocotb, UVM on Verilator). Every service below is delivered as a defined scope with a rerunnable result.

## What we do

| Service | What you get |
|---|---|
| **Coverage hole disposition** | Send the uncovered lines or conditions. For each one you get a formal proof that it is unreachable, a waiver backed by a checked software invariant, or a directed test that reaches it, with the proof log, solver script, or VCD hit count. |
| **Bug reproduction and root cause** | Send the bug report. You get a counterexample trace on the reported RTL, a proof on the fixed RTL, and the mechanism in plain language. Or a not reproduced verdict with the environment condition that explains the report. |
| **RISC-V compliance (ACT4)** | Send the core and its ISA configuration. You get the RISC-V ACT4 compliance suite running on your simulator, the pass and fail table per extension, a triage note on every failure, and the scripts to rerun it on the next revision. |
| **Debug, interrupt, and exception verification** | Properties and tests for single step, debug entry and exit, CSR access in debug, interrupt delivery, and trap ordering. |
| **Formal verification and SVA** | Send the block. You get ten to fifteen design specific properties, each paired with a reachability cover, bound without RTL edits, and proven or bounded with SymbiYosys. |
| **Simulation environments** | cocotb or UVM testbenches with reference models, constrained random stimulus, functional coverage, and self checking. |
| **CDC and async FIFO verification** | Dual clock crossings checked on two independent clocks with data integrity checks. |
| **Verification automation** | Python regression drivers, VCD analysis, watchdogs, result reporting, environment setup scripts. |

## Repositories

| Capability | Repository | Status |
|---|---|---|
| Formal verification | [formal-fsm-verification](https://github.com/Rivoryxa-Technologies/formal-fsm-verification) | Proven by induction with SymbiYosys and z3 |
| SVA checkers | [riscv-sva-library](https://github.com/Rivoryxa-Technologies/riscv-sva-library) | Lints clean under Verilator |
| CDC verification | [cdc-verification](https://github.com/Rivoryxa-Technologies/cdc-verification) | Passes on cocotb 2.x and Icarus Verilog |
| cocotb verification | [cocotb-alu-verification](https://github.com/Rivoryxa-Technologies/cocotb-alu-verification) | Passes on cocotb 2.x and Icarus Verilog |
| UVM verification | [uvm-alu-testbench](https://github.com/Rivoryxa-Technologies/uvm-alu-testbench) | Lints clean under Verilator; runs on a UVM simulator |

## Tools

![Verilator](https://img.shields.io/badge/Verilator-5.x-1f6feb)
![SymbiYosys](https://img.shields.io/badge/SymbiYosys-Yosys%20%7C%20z3%20%7C%20abc-6E4C13)
![cocotb](https://img.shields.io/badge/cocotb-2.x-3776AB?logo=python&logoColor=white)
![UVM](https://img.shields.io/badge/UVM-1.2-1793D1)
![SystemVerilog](https://img.shields.io/badge/SystemVerilog-SVA-EF3B2D)
![ACT4](https://img.shields.io/badge/RISC--V-ACT4%20%7C%20Sail-283272)
![Python](https://img.shields.io/badge/Python-automation-3776AB)

## Scope

We do verification. We do not offer physical design, timing closure, DFT, analog, or silicon bring up, and we say so up front so you know exactly what you are getting.

## Let's talk

If you have an open bug report, a coverage report that will not close, or a core that needs the RISC-V ACT4 compliance suite run on it, send it over.

**LinkedIn:** [Rivoryxa Technologies](https://www.linkedin.com/company/rivoryxa-technologies/)
