# Underflow Bug in Solidity Transfer Function
This repository demonstrates a common underflow bug in Solidity smart contracts and its solution.

The `transfer` function in the `bug.sol` file has an underflow vulnerability. If the `amount` to be transferred exceeds the sender's balance, it will cause an underflow, leading to unexpected behavior or potential exploits.

The `bugSolution.sol` file provides a corrected version of the `transfer` function, using SafeMath to prevent underflow errors.

## How to reproduce the bug
1. Compile `bug.sol` using a Solidity compiler.
2. Deploy the contract to a test network.
3. Attempt to transfer an amount exceeding the sender's balance.
4. Observe the underflow error or unexpected behavior.

## How to fix the bug
1. Use SafeMath library, which provides safe math operations that prevent underflow and overflow errors.