This program acts as a LASM compatible cross-assembler. It is meant to
accept input that is compatible with Ward Christensen's LASM
assembler. It pre-processes asm files to convert the LASM 8080
mnemonics into AS Macroassembler Z80 compatible mnemonics. It then
runs the output through asl and takes the resulting .p file and
converts it to a .hex file.

I have no idea if this thing is useful beyond assembling the CP/M
version of Kermit. I expect there's not much out surviving code out
there that was limited to 8080 mnemonics and was written for ASM or
LASM.

In order to assemble CP/M Kermit 4.11 I had to modify asl to make it
stop erroring out when encountering an END inside of an IF/ENDIF. Once
I did that the output was identical to what I get from LASM running on
CP/M.

Chris Osborn <fozztexx@fozztexx.com>
http://insentricity.com
