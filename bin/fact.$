_EXIT=1
    _PRINTF=127
.SECT .TEXT
start:
    MOV CX,(x)
    DEC CX
    MOV AX,(x)
    CMP AX, 1
    JLE 2f
1:  MUL CX
    LOOP 1b
    JMP 3f

2:  MOV AX,1

!chiamata a sistema per stampare

3:  PUSH AX
    PUSH (x)
    PUSH stampa
    PUSH _PRINTF
    SYS

!chiamata a sistema per uscire
    MOV SP,BP
    PUSH 0
    PUSH _EXIT
    SYS
.SECT .DATA
x: .WORD 4
stampa: .ASCII "Il fattoriale di %d e' %d\n"
.SECT .BSS
