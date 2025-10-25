1.Write an assembly language program in 8086 to find the factorial of a  number and store the result in memory.

AIM

To write an assembly language program in 8086 to find the factorial of a  number and store the result in memory.

APPARATUS REQUIRED

Personal computer

ALGORITHM:
 1: Start the program.
 
 2: Initialize the data segment (DS).
 
 3: Read the input number 
 
 4: Store the number in a register(BL)
 
 5: Initialize another register (AX) with 1 — this will hold the result (factorial).
 
 6: Repeat the following steps until the number becomes zero:
 
 Multiply AX by the current number (BL).
 
 Decrease the number (BL = BL - 1).
 
 7: When BL becomes zero, stop the loop.
 
 8: Store the final result (AX) into memory.
 
 9: Terminate the program.

PROGRAM:

    code segment
    assume cs:code, ds:code
    org 1000h
    mov si, 1200h     
    mov al, [si]      
    mov ah, 00h
    mov bl, al        
    mov ax, 0001h     
    l1: mul bl         
    dec bl             
    jnz l1             
    mov [si+02h], ax   
    mov ah, 4ch
    int 21h
    code ends
    end

OUTPUT

<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/b6658732-9115-42ad-9d5f-24d8b7819143" />
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/15dec09e-7d83-45d0-90e2-c188cf5c32d8" />

MANUAL CALCULATION

<img width="1280" height="576" alt="image" src="https://github.com/user-attachments/assets/b8a446b3-dceb-4b16-b4d7-80cbca45d82a" />

RESULT

Thus, the Assembly Language Programs for 8086 to  find the factorial of a  number and store the result in memory were successfully written and executed using MASM.


