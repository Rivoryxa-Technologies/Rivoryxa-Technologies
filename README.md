# Rivoryxa Technologies

RTL verification for semiconductor and RISC-V teams. We investigate design bugs, coverage gaps, and design rules, with evidence your team can inspect and rerun.

We agree the question, inputs, deliverables, and completion criteria before work starts. When a check cannot establish an answer, we record the remaining uncertainty and the next step.

## Explore the work

These are public educational demonstrations, not client results or production IP. Each repository states its environment and limitations. A deliberately introduced bug is labelled as such.

| Problem to explore | Repository | Evidence to inspect |
| --- | --- | --- |
| A timer interrupt disappears after its compare value | [RISC-V machine timer](https://github.com/Rivoryxa-Technologies/riscv-mtimer-verification) | Seeded failure, simulation, formal counterexample, checked correction, and coverage dispositions |
| A random test misses corruption when a FIFO fills | [Asynchronous FIFO](https://github.com/Rivoryxa-Technologies/cdc-verification) | Directed failure on a seeded variant and passing functional tests at three clock pairs |
| A receiver pauses while data is waiting | [Ready/valid buffer](https://github.com/Rivoryxa-Technologies/ready-valid-verification) | Data stability, ordered transfers, backpressure, and a detected seeded defect |
| Reset arrives while requests are still pending | [Reset recovery](https://github.com/Rivoryxa-Technologies/reset-recovery-verification) | Flush contract, recovery, and detection of a stale response |
| One requester keeps losing access to a shared resource | [Round robin arbitration](https://github.com/Rivoryxa-Technologies/round-robin-verification) | Grant safety and bounded waiting in accepted grants, tested against a fixed priority mutant |
| A controller must keep two directions mutually exclusive | [Formal FSM](https://github.com/Rivoryxa-Technologies/formal-fsm-verification) | Safety proof and reachability checks under the documented model |
| A testbench needs to predict the correct answer | [Python ALU testbench](https://github.com/Rivoryxa-Technologies/cocotb-alu-verification) | Reference model, directed and random tests, and operation counts |

Start with the README in a repository. It explains the problem, reproduction command, recorded results, and limits. The new buffer, reset, and arbiter projects include automated runs, measured tool times, and contribution instructions. Tool runtimes are not client delivery estimates. Scenario counts are not code coverage or proof of all behaviour.

## Services supported by these examples

- **Bug reproduction and root cause:** a replayable failure when one can be found, a cause analysis, and checks of a proposed correction.
- **Coverage closure:** investigate gaps and record directed tests, proofs, supported waivers, or unresolved outcomes.
- **Formal verification and SVA:** design properties, assumptions, counterexamples, proof scope, and reachability checks.
- **Simulation environments:** stimulus, reference models, automatic checking, and reported coverage for an agreed scope.
- **Asynchronous FIFO verification:** functional checks for loss, duplication, and reordering across the tested clocks and reset conditions. This does not replace structural CDC analysis or electrical sign off.

## Reference code with limited evidence

The [SVA library](https://github.com/Rivoryxa-Technologies/riscv-sva-library) and [UVM ALU environment](https://github.com/Rivoryxa-Technologies/uvm-alu-testbench) are code references. Their documented lint results do not establish a formal proof or a completed UVM simulation.

## Reproduce or contribute

Open an issue with the repository revision, tool versions, command, expected behaviour, and actual log. For a proposed correction, include a test that fails before the change and passes after it. Do not upload proprietary RTL or client information to these public repositories.

Confidential work begins with an agreed scope, NDA, and source exchange process.

[Discuss a verification problem by email](mailto:rivoryxatechnologies@gmail.com) · [LinkedIn](https://www.linkedin.com/company/rivoryxa-technologies/)
