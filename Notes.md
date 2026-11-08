
# Hacking: the Art of Exploitation
[The book](https://archive.org/details/HackingTheArtOfExploitation/page/n38/mode/1up) p.38
x86 assembly language syntax: the Intel syntax 
gdb debugger: gdb -q ./a.out
(gdb) break main
setting breakpoint on the main(), execution will stop right before our code is executed
### General purpose registers
- EAX(Accumulator), ECA(Counter), EDX(Data), EBX(Base), mainly act as temp vars for CPU when it is executing machine instructions
- ESP(Stack Pointer) EBP(Base Pointer) ESI(Source Index) EDI(Destination Index), first two store 32-bit addresses, important to program execution and Memory Management, last two commonly used to point to src and dst when data needs to be read from or written to.
- EIP: Instruction Pointer, points to the current instruction the processor is reading.

> Written with [StackEdit](https://stackedit.io/).

<!--stackedit_data:
eyJoaXN0b3J5IjpbNzcxOTQ2Mzc4XX0=
-->