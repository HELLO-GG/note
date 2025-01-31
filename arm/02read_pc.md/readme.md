
### PC寄存器

1. thumb模式读PC寄存器

```asm
mov r0, pc ; thumb mode r0 = pc + 4
```

![20211123161050](https://cdn.jsdelivr.net/gh/yhnu/PicBed/20211123161050.png)

```asm
LDR             R1, =(aLd - 0xAC3B62C)
ADD             R1, PC                  ; "%ld\n"
```

![20211123155731](https://cdn.jsdelivr.net/gh/yhnu/PicBed/20211123155731.png)

2. thumb模式使用LDR使用PC进行间接寻址

如果pc为非4字节对齐, pc会向上对齐

2. arm模式读PC寄存器

```asm
mov r0, pc ; arm mode r0 = pc + 8
```

![20211123170732](https://cdn.jsdelivr.net/gh/yhnu/PicBed/20211123170732.png)

```asm
ldr r0, [pc, #2] ; r0 = mem(pc + 8 + offset(2))
```

![20211123172421](https://cdn.jsdelivr.net/gh/yhnu/PicBed/20211123172421.png)