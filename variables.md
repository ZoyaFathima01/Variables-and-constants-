section .text
        global _start

_start:
        ;======== write your code below ===========
        mov eax, [var1]      ; Load the value of var1 (10) into eax
        mov ebx, [var2]      ; Load the value of var2 (15) into ebx
        add eax, ebx         ; Add eax and ebx, result stays in eax
        mov [result], eax    ; Store the result in memory (result)
        ;======== write your code above ===========

        mov eax,1	        ; set eax register to 1 (do not remove this line)
        int 0x80	        ; interrupt 0x80 (do not remove this line)

segment .bss
        result resd 1        ; Uninitialized variable (1 double word)

segment .data
        var1 dd 10           ; Initialized variable with value 10
        var2 dd 15           ; Initialized variable with value 15
