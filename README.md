# VGA-mode13h

A bootable VGA mode13h *Graphics Programming* in assembly without BIOS interrupts. This code runs on IBM PC compatible operating systems or CSM-supported machines



BOOT.ASM:
The Boot Loader of all system.

TANKI.ASM:
A mini TANK game for fun.

Technical Information About TANKI:
-

*TANKI uses x87 FPU

*TANKI finds coordinates(Trajectory) with following formulas:

*x = v0*(SQRT(2*H/G)

*y = v0*T^2 - GT^2/2

*Tanki uses IBM PC Speaker for voice effect

For Assembling Use NASM(The Netwide Assembler) following commands:
-
nasm -fbin TANKI.asm -o TANKI.bin



nasm -fbin BOOT.asm -o BOOT.bin

(assuming you have created HDD img called file.img)

dd if=BOOT.bin of=file.img conv=notrunc




dd if=TANKI.bin of=file.img seek=1 conv=notrunc

For Emulator Use QEMU with following command:
-
qemu-system-i386 -drive format=raw,file=file.img,index=0,media=disk


It works on REAL x86 HARDWARE too
-
All you need is VGA Compatible hardware/GPU or IBM PC
