# case 3 - Incremental Debugging and Architecture Migration - Blocking-to-Asynchronous Communication Migration

## Usage

This workflow uses the AI as a systems-engineering adviser when an architectural change causes an unclear hardware or communication failure. Instead of replacing the whole blocking implementation with an asynchronous design at once, the AI recommends returning to a known-good baseline and migrating in small, testable steps.

Typical sequence:

1. State the observed symptom and explain why the root cause is uncertain.
2. Identify a previously verified baseline that can be restored.
3. Freeze protocol, CRC, frame parsing, logging, and visible hardware behavior.
4. Change one mechanism at a time and define an acceptance test for each change.
5. Introduce timeouts, then a polling state machine, then interrupt/DMA reception.
6. Perform deeper queue or buffer optimizations only after the data path is stable.

## Approximate Conversation Translation

**User:** The asynchronous communication LED does not light, and we cannot locate the fault. Let us return to the blocking version, which has already been verified, and then change the architecture slowly. Each step should have an acceptance result so that the problem remains traceable. We should not perform a large refactor immediately.

**AI:** I completely agree. This is a typical systems-engineering containment strategy: return to the stable blocking baseline and evolve through small, verifiable steps. A large asynchronous rewrite can simultaneously introduce protocol, state-machine, buffer, timing, ISR, and callback errors.

**AI:** First freeze the protocol, CRC, sequence handling, request/result behavior, LED behavior, and log format. The baseline must remain reproducible. Next, replace the infinite receive wait with a finite timeout without changing anything else. Then add a non-blocking polling skeleton with states such as `IDLE`, `WAIT`, `GOT_FRAME`, and `HANDLE`, while still using a short blocking read in the wait state.

**AI:** After that, replace only the low-level buffer-filling method with interrupt or DMA reception. Reuse the same parser, CRC, and frame assembly logic. The acceptance criterion is: a complete valid frame is parsed and lights the LED as expected; a bad CRC frame is discarded without destabilizing the system. Queue, ring-buffer, double-buffer, or event-driven optimization should be the final step.
