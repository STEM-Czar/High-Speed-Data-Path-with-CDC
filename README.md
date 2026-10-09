# High-Speed-Data-Path-with-CDC
The task is to implement the data movement portion of a modern SoC subsystem in which data must safely cross between independently clocked processing and interface domains.

### Phase 1 | Fundamentals
- [ ] Learn how an asynchronous FIFO works and why it is used between independent clock domains.
- [ ] Learn how binary read and write pointers track FIFO positions.
- [ ] Learn why binary pointers cannot be safely transferred directly across clock domains.
- [ ] Learn how Gray code allows FIFO pointers to cross clock domains safely.
- [ ] Learn how FIFO full and empty conditions are detected.
- [ ] Learn how two flop synchronizers contain metastability when control information crosses clock domains.

### Phase 2 | Architecture and CDC Design
- [ ] Identify every clock domain crossing in the FIFO architecture.
- [ ] Separate the CDC crossings into data paths and control paths.
- [ ] Design the FIFO architecture with independent write and read clock domains.
- [ ] Create a CDC architecture diagram showing every crossing and synchronizer.

### Phase 3 | RTL Implementation
- [ ] Create the parameterized FIFO storage array for 32 bit data.
- [ ] Create the binary write pointer and write address logic.
- [ ] Create the binary read pointer and read address logic.
- [ ] Create the Gray coded write pointer.
- [ ] Create the Gray coded read pointer.
- [ ] Create the write side pointer synchronizer.
- [ ] Create the read side pointer synchronizer.
- [ ] Design the FIFO full detection logic.
- [ ] Design the FIFO empty detection logic.
- [ ] Design the write interface using `wr_valid` and `wr_ready`.
- [ ] Design the read interface using `rd_valid` and `rd_ready`.
- [ ] Create the reset behavior for both clock domains.

### Phase 4 | Functional Verification
- [ ] Create a basic testbench with independent write and read clocks.
- [ ] Test the FIFO with different write and read clock frequencies.
- [ ] Test the FIFO with different clock phase relationships.
- [ ] Test continuous writes until the FIFO becomes full.
- [ ] Test continuous reads until the FIFO becomes empty.
- [ ] Test simultaneous reads and writes.
- [ ] Test reset while the FIFO is empty.
- [ ] Test reset while the FIFO contains data.
- [ ] Add randomized traffic to the testbench.
- [ ] Create a reference model that checks every value entering and leaving the FIFO.

### Phase 5 | Assertions and Waveform Analysis
- [ ] Add assertions for full and empty behavior.
- [ ] Add assertions for valid and ready handshake behavior.
- [ ] Add assertions to detect invalid reads and writes.
- [ ] Generate waveforms showing pointer synchronization and FIFO status changes.
- [ ] Analyze the waveforms to verify that CDC control signals cross through the synchronizers.

Phase 6 | CDC Analysis
- [ ] Write CDC notes explaining why each crossing is safe.


### Phase 7 | Synthesis and Static Timing Analysis
- [ ] Synthesize the FIFO RTL and record area and cell statistics.
- [ ] Create separate timing constraints for the write and read clocks.
- [ ] Declare the write and read clocks asynchronous to each other.
- [ ] Apply appropriate CDC timing exceptions.
- [ ] Run STA and verify that asynchronous CDC paths are not analyzed as normal synchronous paths.
- [ ] Examine timing reports for the remaining synchronous logic.

### Phase 8 | Final Documentation
- [ ] Document the final RTL, verification, CDC analysis, synthesis results, and STA results.
