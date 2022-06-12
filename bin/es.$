_EXIT=1
    _PRINTF=127
.SECT .TEXT
start:
    MOV CX,end1-vec1
    SHR CX,1
    MOV AX,end2-vec2
    SHR AX,1
    CMP AX,CX
    JNE 1f
    MOV SI,vec1
    MOV DI,vec2
    CLD
    REPE CMPSW
    JNE 1f
    PUSH uguali
    JMP 2f
1:  PUSH diversi
2:  PUSH _PRINTF
    SYS
    MOV SP,BP
    PUSH 1
    PUSH _EXIT
    SYS
.SECT .DATA
vec1: .WORD 3,4,7,11,3
end1: .SPACE 1
vec2: .WORD 3,4,7,11,3
end2: .SPACE 1
uguali: .ASCIZ "Uguali!\n"
!con .ASCIZ stiamo inserendo un \0 alla fine di ogni stringa
diversi: .ASCIZ "Diversi!\n"
.SECT .BSS
