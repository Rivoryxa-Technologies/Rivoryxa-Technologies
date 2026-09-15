# Rivoryxa Technologies

RTL verification for semiconductor and RISC-V teams. We investigate design bugs, coverage gaps, and design rules, with evidence your team can inspect and rerun.

We agree the question, inputs, deliverables, and completion criteria before work starts. When a check cannot establish an answer, we record the remaining uncertainty and the next step.

## Explore the work

These are public educational demonstrations, not client results or production IP. Each repository states its environment and limitations. A deliberately introduced bug is labelled as such.

| Problem to explore | Repository | Evidence to inspect |
| --- | --- | --- |
| Architectural tests must match the core configuration | [RISC-V ACT4 integration](https://github.com/Rivoryxa-Technologies/riscv-act4-verification) | Fresh generation and 94 named RTL test results for pinned CV32E40P v2 RV32IMC; not general certification |
| FIFO pointers or synchronizer staging change incorrectly | [Bound FIFO assertions](https://github.com/Rivoryxa-Technologies/fifo-assertion-verification) | Executed SVA at three clock pairs, required exercise counts, and detected negative controls |
| Debug halt and a qualified interrupt arrive together | [RISC-V debug and interrupts](https://github.com/Rivoryxa-Technologies/riscv-debug-interrupt-verification) | Actual pinned CV32E40P controller, directed halt/resume, single-step and exception-priority checks, and two detected priority mutants |
| A regression reports success with incomplete evidence | [Verification automation](https://github.com/Rivoryxa-Technologies/verification-automation) | Complete result matrices from three pinned RTL projects, source hashes, failure handling, and CI |
| A timer interrupt disappears after its compare value | [RISC-V machine timer](https://github.com/Rivoryxa-Technologies/riscv-mtimer-verification) | Seeded failure, simulation, formal counterexample, checked correction, and coverage dispositions |
| A random test misses corruption when a FIFO fills | [Asynchronous FIFO](https://github.com/Rivoryxa-Technologies/cdc-verification) | Directed failure on a seeded variant and passing functional tests at three clock pairs |
| A receiver pauses while data is waiting | [Ready/valid buffer](https://github.com/Rivoryxa-Technologies/ready-valid-verification) | Data stability, ordered transfers, backpressure, and a detected seeded defect |
| Reset arrives while requests are still pending | [Reset recovery](https://github.com/Rivoryxa-Technologies/reset-recovery-verification) | Flush contract, recovery, and detection of a stale response |
| One requester keeps losing access to a shared resource | [Round robin arbitration](https://github.com/Rivoryxa-Technologies/round-robin-verification) | Grant safety and bounded waiting in accepted grants, tested against a fixed priority mutant |
| A controller must keep two directions mutually exclusive | [Formal FSM](https://github.com/Rivoryxa-Technologies/formal-fsm-verification) | Safety proof and reachability checks under the documented model |
| UVM classes need to run and detect a wrong result | [Executed UVM ALU](https://github.com/Rivoryxa-Technologies/uvm-execution-verification) | Three seeds with 200 scoreboard matches each, plus a detected injected mismatch; no class-covergroup coverage claim |
| A testbench needs to predict the correct answer | [Python ALU testbench](https://github.com/Rivoryxa-Technologies/cocotb-alu-verification) | Reference model, directed and random tests, and operation counts |

Start with the README in a repository. It explains the problem, reproduction command, recorded results, and limits. The new buffer, reset, and arbiter projects include automated runs, measured tool times, and contribution instructions. Tool runtimes are not client delivery estimates. Scenario counts are not code coverage or proof of all behaviour.

## Services supported by these examples

- **RISC-V verification:** investigate a defined architectural or subsystem requirement, with the tested configuration and limits recorded.
- **RISC-V architectural tests (ACT4):** pinned test generation, simulator integration, and a complete result matrix for the agreed core configuration.
- **Debug, interrupt, and exception verification:** directed checks of agreed control interactions. The public controller example does not establish whole-core debug compliance or CSR masking behaviour.
- **Verification automation:** reproducible regression execution and validation of complete, current evidence.
- **Bug reproduction and root cause:** a replayable failure when one can be found, a cause analysis, and checks of a proposed correction.
- **Coverage closure:** investigate gaps and record directed tests, proofs, supported waivers, or unresolved outcomes.
- **Formal verification and SVA:** design properties, assumptions, counterexamples, proof scope, and reachability checks.
- **Simulation environments:** cocotb or UVM stimulus, reference models, automatic checking, and supported coverage or scenario reports for an agreed scope.
- **Asynchronous FIFO verification:** functional checks for loss, duplication, and reordering across the tested clocks and reset conditions, plus bound pointer and synchronizer assertions where agreed. This does not replace structural CDC analysis or electrical sign off.

## Reference code with limited evidence

The [SVA library](https://github.com/Rivoryxa-Technologies/riscv-sva-library) remains a code reference with lint results, not a completed formal proof. The [original UVM ALU source](https://github.com/Rivoryxa-Technologies/uvm-alu-testbench) now links to the separate pinned execution runner above, which documents its simulator compatibility and coverage limitations.

## Reproduce or contribute

Open an issue with the repository revision, tool versions, command, expected behaviour, and actual log. For a proposed correction, include a test that fails before the change and passes after it. Do not upload proprietary RTL or client information to these public repositories.

Confidential work begins with an agreed scope, NDA, and source exchange process.

[Discuss a verification problem by email](mailto:rivoryxatechnologies@gmail.com) · [LinkedIn](https://www.linkedin.com/company/rivoryxa-technologies/)
