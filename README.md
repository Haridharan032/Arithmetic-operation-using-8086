# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200: 12               |  1204: 24                |
| ----------------------- | ------------------------ |
|  1201:34                |  1205: 68                |
| ----------------------- | ------------------------ |
|  1202: 12               |  1206: 00                |
| ----------------------- | ------------------------ |
|  1203: 34               |  1207 C4                 |
| ----------------------- | ------------------------ |


#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 30 02_1af7f419](https://github.com/user-attachments/assets/d9fede91-f7e1-4cd8-a387-c61a19b50ec8)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="635" height="394" alt="Screenshot 2025-09-01 184934" src="https://github.com/user-attachments/assets/724152a3-4d6f-43f9-8c08-931456e28572" />


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200: 12               |  1204: 00                |
| ----------------------- | ------------------------ |
|  1201:34                |  1205: 00                |
| ----------------------- | ------------------------ |
|  1202: 12               |  1206: 00                |
| ----------------------- | ------------------------ |
|  1203: 34               |  1207 C4                 |
| ----------------------- | ------------------------ |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 30 01_01650c3d](https://github.com/user-attachments/assets/330add11-8c5d-41de-a212-b1f6b822e173)

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="634" height="397" alt="Screenshot 2025-09-01 185104" src="https://github.com/user-attachments/assets/32e5b9f6-1019-4bbe-873f-7bd4f6320939" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200: 12               |  1204: 44                |
| ----------------------- | ------------------------ |
|  1201:34                |  1205: 51                |
| ----------------------- | ------------------------ |
|  1202: 12               |  1206: 97                |
| ----------------------- | ------------------------ |
|  1203: 34               |  1207: 0A                |
| ----------------------- | ------------------------ |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 30 01_4a0ea776](https://github.com/user-attachments/assets/20626a1a-3fd7-46af-b202-7bdb972e508a)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="636" height="397" alt="Screenshot 2025-09-01 185343" src="https://github.com/user-attachments/assets/8486a962-aeb6-4f7c-a6b9-d3a24b0fcac4" />


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200: 12               |  1204: 01                |
| ----------------------- | ------------------------ |
|  1201:34                |  1205: 00                |
| ----------------------- | ------------------------ |
|  1202: 12               |  1206: 00                |
| ----------------------- | ------------------------ |
|  1203: 34               |  1207: 00                |
| ----------------------- | ------------------------ |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 19 30 01_eb4bac92](https://github.com/user-attachments/assets/889eba3e-c54c-4082-a2a9-0ac02d71aed6)

---
## OUTPUT FROM MASM SOFTWARE

<img width="637" height="390" alt="Screenshot 2025-09-01 185755" src="https://github.com/user-attachments/assets/26f55f53-3ade-4082-b0c5-8732dcd9a484" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
