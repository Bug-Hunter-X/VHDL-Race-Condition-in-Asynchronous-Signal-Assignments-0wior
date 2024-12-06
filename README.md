# VHDL Race Condition Example

This repository demonstrates a potential race condition in VHDL code.  The `bug.vhdl` file contains a simple design with a process that updates signals.  Due to the way the assignments are structured, there's a possibility of a race condition leading to incorrect output under certain circumstances.  The `bugSolution.vhdl` file shows how this can be corrected.

## Bug Description

The race condition can occur because the assignments to `internal_data` and `data_out` within the process are not explicitly sequenced to avoid the possibility that the two assignments are not fully completed before the next clock edge.

## Solution

The solution involves using better signal assignments to avoid potential concurrency issues within the `process`.  This ensures predictable and reliable operation.
