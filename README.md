# ASMnutshell
This repository serves as a reference guide for x86 assembly language, providing information about registers and common instructions.

## INSTRUCTIONS
```assembly
; Data Movement Instructions
mov  : Move                   : Copies the value of one operand to another.
lea  : Load Effective Address : Calculates the effective address of the source operand and loads it into the destination operand.

; Arithmetic and Logic Instructions
add  : Add            : Adds the values of two operands.
sub  : Subtract       : Subtracts the value of the second operand from the first.
mul  : Multiply       : Multiplies the values of two operands.
div  : Divide         : Divides the value of the first operand by the second.
inc  : Increment      : Increases the value of the operand by 1.
dec  : Decrement      : Decreases the value of the operand by 1.
cmp  : Compare        : Compares the values of two operands.
xor  : Exclusive OR   : Performs bitwise exclusive OR on two operands.
and  : Bitwise AND    : Performs bitwise AND on two operands.
or   : Bitwise OR     : Performs bitwise OR on two operands.
not  : Bitwise NOT    : Performs bitwise NOT on an operand.
shl  : Shift Left     : Shifts the bits of the destination operand to the left.
shr  : Shift Right    : Shifts the bits of the destination operand to the right.

; Control Transfer Instructions
jmp  : Jump                     : Unconditionally jumps to a specified address.
je   : Jump if Equal            : Jumps to a specified address if the zero flag is set (equal).
jne  : Jump if Not Equal        : Jumps to a specified address if the zero flag is not set (not equal).
jl   : Jump if Less             : Jumps to a specified address if the sign flag is set (less than).
jg   : Jump if Greater          : Jumps to a specified address if the zero flag is not set and the sign flag is not equal to the overflow flag (greater than).
jle  : Jump if Less or Equal    : Jumps to a specified address if the zero flag is set or the sign flag is set (less than or equal).
jge  : Jump if Greater or Equal : Jumps to a specified address if the zero flag is set and the sign flag is not set (greater than or equal).

; String Instructions
cmpsb : Compare Strings Byte         : Compares two strings byte-by-byte.
cmpsw : Compare Strings Word         : Compares two strings word-by-word.
cmpsd : Compare Strings Doubleword   : Compares two strings doubleword-by-doubleword.
lodsb : Load String Byte             : Loads a byte from the source string into AL.
lodsw : Load String Word             : Loads a word from the source string into AX.
lodsd : Load String Doubleword       : Loads a doubleword from the source string into EAX.
stosb : Store String Byte            : Stores a byte from AL into the destination string.
stosw : Store String Word            : Stores a word from AX into the destination string.
stosd : Store String Doubleword      : Stores a doubleword from EAX into the destination string.

; Stack Instructions
push : Push           : Pushes the value onto the stack.
pop  : Pop            : Removes the top value from the stack and stores it.

; Miscellaneous Instructions
nop  : No Operation   : Does nothing and is often used as a placeholder.
call : Call Procedure : Pushes the address of the next instruction onto the stack and transfers control to a specified procedure.
ret  : Return         : Pops the top of the stack into the instruction pointer, transferring control back to the calling procedure.
```
```assembly
; Uncommon x86 Assembly Instructions
bsf    : Bit Scan Forward                                    : Finds the position of the first set bit (1) in the source operand and stores the result in the destination operand.
bsr    : Bit Scan Reverse                                    : Finds the position of the last set bit (1) in the source operand and stores the result in the destination operand.
bt     : Bit Test                                            : Tests the bit at a specified position in the source operand and sets the zero flag accordingly.
btc    : Bit Test and Complement                             : Tests and complements the bit at a specified position in the source operand.
btr    : Bit Test and Reset                                  : Tests and resets (clears) the bit at a specified position in the source operand.
bts    : Bit Test and Set                                    : Tests and sets the bit at a specified position in the source operand.
xadd   : Exchange and Add                                    : Exchanges the destination operand with the source operand, then adds the source operand to the destination operand.
xchg   : Exchange                                            : Exchanges the values of two operands.
cmova  : Conditional Move if Overflow                        : Moves the contents of the source operand to the destination operand if the overflow flag is set.
cmovb  : Conditional Move if Below (carry flag set)          : Moves the contents of the source operand to the destination operand if the carry flag is set.
cmovbe : Conditional Move if Below or Equal (CF=1 or ZF=1)   : Moves the contents of the source operand to the destination operand if the carry flag is set or the zero flag is set.
cmovg  : Conditional Move if Greater (ZF=0 and SF=OF)        : Moves the contents of the source operand to the destination operand if the zero flag is not set and the sign flag equals the overflow flag.
cmovge : Conditional Move if Greater or Equal (SF=OF)        : Moves the contents of the source operand to the destination operand if the sign flag equals the overflow flag.
cmovl  : Conditional Move if Less (SF ≠ OF)                  : Moves the contents of the source operand to the destination operand if the sign flag is not equal to the overflow flag.
cmovle : Conditional Move if Less or Equal (ZF=1 or SF ≠ OF) : Moves the contents of the source operand to the destination operand if the zero flag is set or the sign flag is not equal to the overflow flag.
cmovno : Conditional Move if Not Overflow                    : Moves the contents of the source operand to the destination operand if the overflow flag is not set.
cmovnp : Conditional Move if Not Parity                      : Moves the contents of the source operand to the destination operand if the parity flag is not set.
cmovns : Conditional Move if Not Sign                        : Moves the contents of the source operand to the destination operand if the sign flag is not set.
cmovnz : Conditional Move if Not Zero                        : Moves the contents of the source operand to the destination operand if the zero flag is not set.
cmovo  : Conditional Move if Overflow                        : Moves the contents of the source operand to the destination operand if the overflow flag is set.
cmovp  : Conditional Move if Parity                          : Moves the contents of the source operand to the destination operand if the parity flag is set.
cmovs  : Conditional Move if Sign                            : Moves the contents of the source operand to the destination operand if the sign flag is set.
cmovz  : Conditional Move if Zero                            : Moves the contents of the source operand to the destination operand if the zero flag is set.
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
