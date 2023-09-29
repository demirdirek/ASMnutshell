# ASMnutshell
This repository serves as a reference guide for x86 assembly language, providing information about registers and common instructions.

## INSTRUCTIONS
```assembly
; Arithmetic Instructions
add   : Add          : Adds the values of two operands.
sub   : Subtract     : Subtracts the value of the second operand from the first.
mul   : Multiply     : Multiplies the values of two operands.
div   : Divide       : Divides the value of the first operand by the second.

; Logical Instructions
and   : Bitwise AND  : Performs bitwise AND on two operands.
or    : Bitwise OR   : Performs bitwise OR on two operands.
xor   : Exclusive OR : Performs bitwise exclusive OR on two operands.
not   : Bitwise NOT  : Performs bitwise NOT on an operand.

; Comparison Instructions
cmp   : Compare      : Compares the values of two operands.

; Jump Instructions
jmp   : Jump               : Unconditionally jumps to a specified address.
je    : Jump if Equal      : Jumps if the Zero Flag is set (indicating equality).
jne   : Jump if Not Equal  : Jumps if the Zero Flag is not set (indicating inequality).
js    : Jump if Sign       : Jumps to a specified address if the Sign Flag is set (negative result).

; Stack Instructions
push  : Push       : Pushes the value onto the stack.
pop   : Pop        : Removes the top value from the stack and stores it.

; Other Instructions
mov   : Move       : Copies the value of one operand to another.
inc   : Increment  : Increases the value of the operand by 1.
dec   : Decrement  : Decreases the value of the operand by 1.

; Manipulation Operations
shl  : Shift Left     : Shifts the bits of the destination operand to the left.
shr  : Shift Right    : Shifts the bits of the destination operand to the right.
```
## REGISTERS
```assembly
; General-Purpose Registers:
EAX   : Accumulator            : General-purpose register for arithmetic and data operations.
EBX   : Base                   : General-purpose register often used for addressing.
ECX   : Counter                : General-purpose register often used as a loop counter.
EDX   : Data                   : General-purpose register for data operations.
EBP   : Base Pointer           : Points to the base of the current stack frame.
ESP   : Stack Pointer          : Points to the top of the stack.
ESI   : Source Index           : Used for source data in string operations.
EDI   : Destination Index      : Used for destination data in string operations.
EIP   : Instruction Pointer    : Points to the next instruction to be executed.
EFLAGS: Flags Register         : Contains various status flags (ZF, PF, AF, OF, SF, DF, CF, TF, IF).

; Flags:
ZF    : Zero Flag              : Set if the result of an operation is zero.
OF    : Overflow Flag          : Set if an arithmetic operation produces a result too large.
CF    : Carry Flag             : Set if an arithmetic operation generates a carry out.
PF    : Parity Flag            : Set if the number of set bits is even.
SF    : Sign Flag              : Indicates the sign of the result of an operation.
TF    : Trap Flag              : Used for single-stepping through code.
AF    : Auxiliary Carry Flag   : Used for binary-coded decimal (BCD) arithmetic.
DF    : Direction Flag         : Affects the direction in string operations.
IF    : Interrupt Flag         : If set, interrupts are enabled.

; System Information Registers:
LastError  : Holds the result of the last system call error.
LastStatus : Holds the status of the last system call.

; Segment Registers:
GS, ES, CS, FS, DS, SS: Segment registers used for specifying memory segments.

; Floating Point Registers (x87 FPU):
ST(0) - ST(7)      : Floating-point stack registers used for floating-point arithmetic.
x87TagWord         : Holds information about the contents of the x87 FPU stack registers.
x87ControlWord     : Controls the operation of the x87 FPU.
x87StatusWord      : Provides information about the status of the x87 FPU.
x87TW_0 - x87TW_7  : x87 Tag Word bits for each FPU stack register.
x87SW_B            : Busy flag in x87 Status Word.
x87SW_C3           : Condition Code 3 in x87 Status Word.
x87SW_TOP          : Top of the x87 FPU stack.
x87SW_C2           : Condition Code 2 in x87 Status Word.
x87SW_C1           : Condition Code 1 in x87 Status Word.
x87SW_O            : Overflow flag in x87 Status Word.
x87SW_ES           : Exception Summary in x87 Status Word.
x87SW_SF           : Stack Fault flag in x87 Status Word.
x87SW_P            : Precision flag in x87 Status Word.
x87SW_U            : Underflow flag in x87 Status Word.
x87SW_Z            : Zero divide flag in x87 Status Word.
x87SW_D            : Denormalized operand flag in x87 Status Word.
x87SW_I            : Invalid operation flag in x87 Status Word.
x87SW_C0           : Condition Code 0 in x87 Status Word.

; Control and Status Registers:
MxCsr          : Control and status register for SIMD and floating-point operations.
MxCsr_FZ       : Flush to Zero bit in MxCsr.
MxCsr_PM       : Precision Mask bit in MxCsr.
MxCsr_UM       : Underflow Mask bit in MxCsr.
MxCsr_OM       : Overflow Mask bit in MxCsr.
MxCsr_ZM       : Zero Divide Mask bit in MxCsr.
MxCsr_IM       : Invalid Operation Mask bit in MxCsr.
MxCsr_DM       : Denormals are Zero Mask bit in MxCsr.
MxCsr_DAZ      : Denormals are Zero bit in MxCsr.
MxCsr_PE       : Precision Flag in MxCsr.
MxCsr_UE       : Underflow Flag in MxCsr.
MxCsr_OE       : Overflow Flag in MxCsr.
MxCsr_ZE       : Zero Divide Flag in MxCsr.
MxCsr_DE       : Denormalized Operand Flag in MxCsr.
MxCsr_IE       : Invalid Operation Flag in MxCsr.
MxCsr_RC       : Rounding Control field in MxCsr.

; SIMD Registers (XMM, YMM):
XMM0 - XMM7    : SIMD registers for vectorized operations.
YMM0 - YMM7    : Extended SIMD registers for Advanced Vector Extensions (AVX) operations.

; Debug Registers:
DR0 - DR7      : Debug registers used for hardware breakpoints and debugging.
```
