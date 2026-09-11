<div align="center">
  <img src="https://avatars.githubusercontent.com/Rivoryxa-Technologies" width="130" alt="Rivoryxa Technologies" />

  # Rivoryxa Technologies

  **RISC-V and RTL verification. Formal proofs, bug reproduction, coverage closure, and compliance testing on open tools.**

  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Rivoryxa%20Technologies-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/company/rivoryxa-technologies/)
  ![RISC-V](https://img.shields.io/badge/RISC--V-Verification-283272)
  ![Formal](https://img.shields.io/badge/Formal-SymbiYosys-6E4C13)
  ![OpenHW](https://img.shields.io/badge/OpenHW-Contributor-1f6feb)
</div>

---

Rivoryxa is a verification company. We take a RISC-V core or an RTL block and answer one question with evidence: is this bug real, is this coverage hole reachable, does this core pass the spec. Every result we deliver comes with a reproducible artifact: a proof log, a counterexample trace, a directed test with hit counts, or a certification run.

We work on open-source tools (Verilator, SymbiYosys, Yosys, z3, cocotb, UVM on Verilator), so clients can rerun every proof and every regression without a licence.

## What we deliver

| Service | What you get | Evidence |
|---|---|---|
| **Coverage-hole disposition** | For each uncovered line or condition: an unbounded proof that it is dead, a waiver backed by a machine-checked software invariant, or a directed test that reaches it. | CV32E40P v2 coverage holes: unbounded proof of cv32e40p#1010 (single-step in DECODE_HWLOOP unreachable), z3-checked invariant waiver for cv32e40p#1009, directed hardware-loop tests with VCD hit counts. |
| **Bug reproduction and root cause** | A bug report turned into a counterexample on the reported RTL, a proof on the fixed RTL, and a written mechanism. | Six closed CV32E40X debug and CSR bugs replayed as formal counterexamples on pre-fix RTL and proven fixed on master. cv32e40p#1060 (mstatus.FS timing) independently reproduced from an ACT4 run. |
| **RISC-V compliance (ACT4)** | The RISC-V architectural certification suite brought up on your core, run, and triaged against known issues. | CORE-V Wally: 95/95 rv32imc, 1969/1976 rv64gc (remaining 7 confirmed as known CVW issues by the core's author). CV32E40P: 94/94 rv32imc, 180/181 rv32imcf. |
| **Debug, interrupt, and exception verification** | Properties and tests for single-step, debug entry and exit, CSR access in debug, interrupt delivery, and trap ordering. | The CV32E40X replays above; root cause of a CV32E40P ACT4 interrupt failure (testbench interrupt generator address mismatch), confirmed by the OpenHW maintainer. |
| **Formal verification and SVA** | Assertion suites with anti-vacuity covers, engine escalation (PDR, k-induction, BMC), and OBI or bus assumptions that make proofs converge. | [formal-fsm-verification](https://github.com/Rivoryxa-Technologies/formal-fsm-verification), [riscv-sva-library](https://github.com/Rivoryxa-Technologies/riscv-sva-library), proofs above. |
| **Simulation environments** | cocotb or UVM testbenches with reference models, constrained-random stimulus, functional coverage, and self-checking. | [cocotb-alu-verification](https://github.com/Rivoryxa-Technologies/cocotb-alu-verification), [uvm-alu-testbench](https://github.com/Rivoryxa-Technologies/uvm-alu-testbench). |
| **CDC and async FIFO verification** | Dual-clock crossings checked on two independent clocks with data-integrity proofs. | [cdc-verification](https://github.com/Rivoryxa-Technologies/cdc-verification). |
| **Verification automation** | Python regression drivers, VCD analysis, watchdogs, result JSON, environment bring-up scripts. | ACT4 regressions up to 1976 ELFs; [riscv-dv#1035](https://github.com/chipsalliance/riscv-dv/pull/1035) (Python fix to the CSR test generator, approved). |

## Open-source RISC-V contributions

Our work is upstream and public, authored by our founder Avinash Kollu, an OpenHW Foundation contributor.

- [openhwgroup/cve2#334](https://github.com/openhwgroup/cve2/pull/334), merged: fixes the `$fatal` finish number in the CVE2 core tracing module.
- [openhwgroup/core-v-mcu#371](https://github.com/openhwgroup/core-v-mcu/pull/371), merged: documents the APB Timer as the RISC-V machine timer, including the safe 64-bit `mtimecmp` update sequence.
- [chipsalliance/riscv-dv#1035](https://github.com/chipsalliance/riscv-dv/pull/1035), approved: the CSR test generator no longer emits illegal writes to read-only CSRs.
- RISC-V ACT4 certification runs on CORE-V Wally and CV32E40P, delivered on request of the OpenHW verification lead.

## Cores we have worked on

CV32E40P, CV32E40X, CV32E40S, CVE2, CORE-V Wally, CORE-V-MCU.

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

We do verification. We do not offer physical design, timing closure, DFT, analog, or silicon bring-up, and we say so up front so you know exactly what you are getting.

## Let's talk

If you have an open bug report, a coverage report that will not close, or a core that needs the RISC-V certification suite run on it, send it over.

**LinkedIn:** [Rivoryxa Technologies](https://www.linkedin.com/company/rivoryxa-technologies/)
