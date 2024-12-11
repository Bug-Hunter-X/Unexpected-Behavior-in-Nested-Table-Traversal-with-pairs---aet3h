# Lua Nested Table Traversal Bug

This repository demonstrates a subtle bug in Lua related to table traversal using `pairs()` and modification of tables during iteration.  The `pairs()` iterator does not guarantee a specific order, which can lead to unexpected results when the tables are modified within the iteration process.

The `bug.lua` file contains the buggy code, while `bugSolution.lua` demonstrates a correct solution using a different approach.

## How to reproduce

1. Clone this repository.
2. Run `lua bug.lua`
3. Observe the unexpected output.
4. Run `lua bugSolution.lua` to see the corrected output.

## Solution

The solution involves using a different approach to avoid modifying the table during iteration.  See `bugSolution.lua` for an example.  The key is to process the tables in a way that doesn't alter the table that is being iterated.