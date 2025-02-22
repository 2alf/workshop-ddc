
### Move it

```assembly
mov rax, rdi
mov ebx, DWORD PTR [r8]
mov DWORD PTR [r9], esi
```

### 2 plus 2
```assembly
mov rax, rdi
add rax, rsi
mov bx, WORD PTR[r8]
imul rbx, rdx
sub rax, rbx
mov QWORD PTR[r9], rax
```

### Height check
```assembly
loop:
mov al, BYTE PTR[r8]
cmp al, 0x50
jbe else
sub al, 0x37
jmp join
else:
add al, 0x13
join:
mov BYTE PTR[r9], al
inc r8
inc r9
dec rdi
jnz loop
```