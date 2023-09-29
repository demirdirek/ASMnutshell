# ASMnutshell
You are trying to read an ASM binary but you don't know what the actual hell you looking... SAY LESS MATE!

instructions and their meanings
```
cmp  : Compare        : Compares the values of two operands.
js   : Jump if Sign   : Jumps to a specified address if the sign flag is set.
xor  : Exclusive OR   : Performs bitwise exclusive OR on two operands.
inc  : Increment      : Increases the value of the operand by 1.
jmp  : Jump           : Unconditionally jumps to a specified address.
mov  : Move           : Copies the value of one operand to another.
add  : Add            : Adds the values of two operands.
sub  : Subtract       : Subtracts the value of the second operand from the first.
mul  : Multiply       : Multiplies the values of two operands.
div  : Divide         : Divides the value of the first operand by the second.
and  : Bitwise AND    : Performs bitwise AND on two operands.
or   : Bitwise OR     : Performs bitwise OR on two operands.
not  : Bitwise NOT    : Performs bitwise NOT on an operand.
shl  : Shift Left     : Shifts the bits of the destination operand to the left.
shr  : Shift Right    : Shifts the bits of the destination operand to the right.
push : Push           : Pushes the value onto the stack.
pop  : Pop            : Removes the top value from the stack and stores it.
```

registers
```
General-Purpose Registers:
eax  : Accumulator     : General-purpose register for arithmetic and data operations.
ebx  : Base            : General-purpose register often used for addressing.
ecx  : Counter         : General-purpose register often used as a loop counter.
edx  : Data            : General-purpose register for data operations.
ebp  : Base Pointer    : Points to the base of the current stack frame.
esp  : Stack Pointer   : Points to the top of the stack.
esi  : Source Index    : Used for source data in string operations.
edi  : Destination Index: Used for destination data in string operations.
eip  : Instruction Pointer: Points to the next instruction to be executed.
eflags: Flags Register  : Contains various status flags (ZF, PF, AF, OF, SF, DF, CF, TF, IF).

Flags:
ZF   : Zero Flag        : Set if the result of an operation is zero.
PF   : Parity Flag      : Set if the number of set bits is even.
AF   : Auxiliary Carry Flag: Used for binary-coded decimal (BCD) arithmetic.
OF   : Overflow Flag    : Set if an arithmetic operation produces a result too large.
SF   : Sign Flag        : Indicates the sign of the result of an operation.
DF   : Direction Flag   : Affects the direction in string operations.
CF   : Carry Flag       : Set if an arithmetic operation generates a carry out.

Floating Point Registers (x87 FPU):
ST(0), ST(1), ..., ST(7): Floating-point stack registers used for floating-point arithmetic.

SIMD Registers (XMM):
xmm0, xmm1, ..., xmm15 : SIMD (Single Instruction, Multiple Data) registers for vectorized operations.

Vector Registers (AVX):
ymm0, ymm1, ..., ymm15 : Extended SIMD registers for Advanced Vector Extensions (AVX) operations.

System Information Registers:
lasterror             : Holds the result of the last system call error.
laststatus            : Holds the status of the last system call.

Segment Registers:
GS, FS, ES, DS, CS, SS: Segment registers used for specifying memory segments.
```
