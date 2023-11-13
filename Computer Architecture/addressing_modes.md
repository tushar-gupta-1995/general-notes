![Alt text](image-132.png)

# syntax: grammar of TOC (or a rule)

# semantic: the meaning of a statement

![Alt text](image-133.png)

![Alt text](image-134.png)

**Note:**In the above image AC represents accumulator

![Alt text](image-135.png)

![Alt text](image-136.png)

**answer to above:** d

## Instruction set
- represents how many types of instructions can  be run by a machine
- in other words how many different opcodes are there.


# Criteria for addressing modes
![Alt text](image-145.png)

# Immediate Mode: Instruction contains operand

![Alt text](image-146.png)

## Advantages:

![Alt text](image-147.png)

![Alt text](image-148.png)

# Direct/Absolute.Effective Mode: Instruction contains address of operand

![Alt text](image-150.png)

![Alt text](image-151.png)


# Indirect Mode: Instruction contains address of the address that holds the operand

![Alt text](image-154.png)

![Alt text](image-155.png)

# Implied Mode: If address of operand can be deciphered from instruction definition

![Alt text](image-157.png)

# Register Mode addressing

![Alt text](image-158.png)

- Registers are expensive and few in a machine
- instruction tells the register number, but because number of registers are less, the bit to specify the register is also less
- because very limited number of registers are less, cannot be used for every instruction

# Register indriect addressing mode / auto increment addressing mode:

![Alt text](image-159.png)

 - instruction has the number of register that holds the memory address of the variable

 ![Alt text](image-163.png)


 # Base Register

 ![Alt text](image-165.png)

 - instruction contains opcode+base register number + offset
 - register tells base address
 - ALU adds offset to base to get operand for current instruction

 ![Alt text](image-166.png)