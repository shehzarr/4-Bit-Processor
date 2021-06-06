# 4-Bit-Processor

A 4-bit processor which consists of 4 data registers each of 4 bits and an instruction register (IR)
of 7 bits. The processor has four flags ZF, SF, OF and Cout. The first 3 bits of the instruction tells which
operation is to be performed, the next 2 bits signifies the first register and the last two bits signifies the
second register.

I 6 -I 4 I 3 -I 2 I 1 – I 0
Operation Code 4-bit register operand 1(R1)

4-bit register operand 2 (R2)

The following operations are performed by the processor.
Operation Code Operation Performed Description
000 R1 = A Load the contents of input A in to the register operand 1.
001 R1 = R2 Move the contents of register operand 2 in to register operand 1.
010 R1 = R1 + R2 Add the contents of register operand 1 and register operand 2 and

load in register operand 1.

011 R1 = R1 - R2 Subtract the contents of register operand 2 from register operand

1 and load in register operand 1.

100 R1 = R1 * R2 Multiply the contents of register operand 1 and register operand 2
and load in register operand 1 and 2. (As the result is of 8 bits)
101 R1 = R1/2 i Divide the register contents of register operand 1 with 2 i (i is an

input) and load the result in register operand 1.

110 R1 = R1*2 I Multiply the register contents of register operand 1 with 2 i (i is an

input) and load the result in register operand 1.

111 R1 = R1 + R2 Logical OR the contents of register operand 1 and register operand

2 and load in register operand 1.

Functionality of the flags is described below:
Flag Operation Description
ZF All Zero Flag: ZF = 0 if result of current ALU operation is zero and 1 otherwise
SF All Sign Flag: Reflects the most significant bot of the result of current ALU

Operation OF Add/Subtract

Overflow Flag: This bit is one if the current operation caused a two’s complement overflow – either positive or negative, and will be off otherwise Cout Add/Subtract Carry Flag: This bit is 1 if the addition caused a carry-out from the most significant bit position, so an unsigned overflow
<br>
<b>
Inputs: Clock Pulse (CP), 7-bits Instruction, A, i
Output: Contents of each register
