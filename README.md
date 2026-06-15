# VGA-mode13h

A bootable VGA mode13h *Graphics Programming* in assembly without BIOS interrupts. This code runs on IBM PC compatible operating systems or CSM-supported machines



#BOOT.ASM:
-The Boot Loader of all system.

#TANKI.ASM:
-A mini TANK game for fun.

-Technical Information About TANKI:
-
TANKI uses x87 FPU
TANKI finds coordinates(Trajectory) with following formulas:
#x = v0*(SQRT(2*H/G)#
#-y = v0*T^2 - GT^2/2#
