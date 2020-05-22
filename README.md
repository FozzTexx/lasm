This program acts as a LASM compatible cross-assembler. It is meant to
accept input that is compatible with Ward Christensen's LASM
assembler. It pre-processes asm files to convert the ASM/LASM 8080
mnemonics into AS Macroassembler Z80 compatible mnemonics. It then
runs the output through asl and takes the resulting .p file and
converts it to a .hex file.

I've also added a mode to make it accept TASM compatible assembly.

I have no idea if this thing is useful beyond assembling the CP/M
version of Kermit. I expect there's not much surviving code out there
that was limited to 8080 mnemonics and was written for ASM or LASM. I
was able to assemble CP/M 2.2 from the 8080 source too, but since it's
also provided with Z80 mnemonics I'm not sure how useful that is.

In order to assemble CP/M Kermit 4.11 I had to modify asl to make it
stop erroring out when encountering an END inside of an IF/ENDIF. Once
I did that the output was identical to what I get from LASM running on
CP/M.

The version of asl I'm using is at https://github.com/begoon/asl.git
and you can find the patch in 0001-asl-end.patch

http://www.insentricity.com/a.cl/259

Chris Osborn <fozztexx@fozztexx.com>
http://insentricity.com
