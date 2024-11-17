# contract-compilation-code

When we compile a contract, it's typically split up into:
1. Contract Creation Code
2. RunTime Code
3. Metadata (Optional)

We can find the different sections inside the bytecode by looking to see what sections are unreachable. A good way to start is by looking at the RETURN (F3 opcode). Another opcode we can look at is the CODECOPY (39 opcode).

The solidity compiler adds an INVALID (FE opcode) opcode between these three sections to make them easier to locate.
