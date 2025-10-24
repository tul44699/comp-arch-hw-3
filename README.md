## Annotated c to y86 code is contained in y86-code/hw_test.ys


### final output of c code:
```X = 40, Arrays (A, S) = 
(3, 5) (-7, 2125) (0, 2165) (-1, 2245) (-5, 3525) (-2, 3685) (1, 3705) (3, 3710) (-13, 4390) (-4, 5030)
```

### final output of y86 code:
```210 instructions executed
Status = HLT
Condition Codes: Z=0 S=0 O=0
Changed Register State:
%rax:   0x0000000000000000      0x0000000000000001
%rcx:   0x0000000000000000      0xffffffffffffffff
%rdx:   0x0000000000000000      0x0000000000000bb8
%rbx:   0x0000000000000000      0xfffffffffffffffc
%rsp:   0x0000000000000000      0x0000000000000300
%rsi:   0x0000000000000000      0x0000000000000028
%rdi:   0x0000000000000000      0x00000000000001f8
%r8:    0x0000000000000000      0x0000000000000067 // accumulated sum
%r9:    0x0000000000000000      0x0000000000000002
%r10:   0x0000000000000000      0xfffffffffffffffc
%r11:   0x0000000000000000      0xffffffffffffffff
%r14:   0x0000000000000000      0x0000000000000008
Changed Memory State:
0x02f8: 0x0000000000000000      0x0000000000000013
```



### Final iterations (I cannot run the GUI version of the simulator, so I can only look at the yis output)
```
IF: Fetched tjlt at 0x16e.  ra=%r11, rb=----, valC = 0x187
IF: Fetched rrmovq at 0x187.  ra=%rsi, rb=%r9, valC = 0x0
IF: Fetched rrmovq at 0x189.  ra=%rbx, rb=%r10, valC = 0x0
IF: Fetched irmovq at 0x18b.  ra=----, rb=%r11, valC = 0x0
IF: Fetched subq at 0x195.  ra=%r10, rb=%r11, valC = 0x0
IF: Fetched shaq at 0x197.  ra=%r11, rb=%r9, valC = 0x0
IF: Fetched rrmovq at 0x199.  ra=%r9, rb=%r12, valC = 0x0
IF: Fetched divq at 0x19b.  ra=%rdx, rb=%r12, valC = 0x0
IF: Fetched mulq at 0x19d.  ra=%rdx, rb=%r12, valC = 0x0
IF: Fetched subq at 0x19f.  ra=%r12, rb=%r9, valC = 0x0
IF: Fetched tjge at 0x1a1.  ra=%r9, rb=----, valC = 0x1ad
IF: Fetched addq at 0x1ad.  ra=%r9, rb=%r8, valC = 0x0
IF: Fetched jmp at 0x1af.  ra=----, rb=----, valC = 0x148
IF: Fetched rrmovq at 0x148.  ra=%rcx, rb=%r11, valC = 0x0
IF: Fetched tjlt at 0x14a.  ra=%r11, rb=----, valC = 0x1b8
IF: Fetched ret at 0x1b8.  ra=----, rb=----, valC = 0x0
IF: Fetched halt at 0x13.  ra=----, rb=----, valC = 0x0
210 instructions executed
```
