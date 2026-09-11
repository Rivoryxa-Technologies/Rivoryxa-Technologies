<div align="center">
  <img src="https://avatars.githubusercontent.com/Rivoryxa-Technologies" width="130" alt="Rivoryxa Technologies" />

  # Rivoryxa Technologies

  **RISC-V and RTL verification. Formal proofs, bug reproduction, coverage closure, and compliance testing on open tools.**

  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Rivoryxa%20Technologies-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/company/rivoryxa-technologies/)
  ![RISC-V](https://img.shields.io/badge/RISC--V-Verification-283272)
  ![Formal](https://img.shields.io/badge/Formal-SymbiYosys-6E4C13)
</div>

---

Rivoryxa is a verification company. We take a RISC-V core or an RTL block and answer one question with evidence: is this bug real, is this coverage hole reachable, does this core pass the spec. Every result we deliver comes with a reproducible artifact: a proof log, a counterexample trace, a directed test with hit counts, or a certification run.

We work on open source tools (Verilator, SymbiYosys, Yosys, z3, cocotb, UVM on Verilator), so clients can rerun every proof and every regression without a licence.

## What we do

| Service | What you get |
|---|---|
| **Coverage hole disposition** | For each uncovered line or condition: a formal proof that it is dead, a waiver backed by a checked software invariant, or a directed test that reaches it. |
| **Bug reproduction and root cause** | A bug report turned into a counterexample on the reported RTL, a proof on the fixed RTL, and a written mechanism. |
| **RISC-V compliance (ACT4)** | The RISC-V architectural certification suite brought up on your core, run, and triaged. |
| **Debug, interrupt, and exception verification** | Properties and tests for single step, debug entry and exit, CSR access in debug, interrupt delivery, and trap ordering. |
| **Formal verification and SVA** | Assertion suites with reachability covers and engine escalation (PDR, induction, BMC). |
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

If you have an open bug report, a coverage report that will not close, or a core that needs the RISC-V certification suite run on it, send it over.

**LinkedIn:** [Rivoryxa Technologies](https://www.linkedin.com/company/rivoryxa-technologies/)
