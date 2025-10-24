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
|         2000-44         |          2004-99         |
|         2001-44         |          2005-99         |
|         2002-55         |                          |
|         2003-55         |                          |

#### Manual Calculations

![IMG-20251024-WA0008 1](https://github.com/user-attachments/assets/90284e82-3c41-47bf-9ffe-07f9ccbcd24d)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="637" height="431" alt="Screenshot 2025-09-19 075144" src="https://github.com/user-attachments/assets/289afe13-2609-4a9c-ae85-7100ecaec81d" />

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
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
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
|        2000-99          |         2004-44          |
|        2001-99          |         2005-44          |
|        2002-55          |                          |
|        2003-55          |                          |

#### Manual Calculations

![IMG-20251024-WA0014 1](https://github.com/user-attachments/assets/4ac05c07-efeb-407f-9727-4a4d93589be3)

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="635" height="432" alt="image" src="https://github.com/user-attachments/assets/1b988584-774e-433e-86e4-b4e2a2851f24" />

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
|    2000-22              |          2005-42         |
|    2001-22              |          2006-86         |
|    2002-11              |          2007-46         |
|    2003-11              |          2008-02         |
#### Manual Calculations

![IMG-20251024-WA0016 1](https://github.com/user-attachments/assets/a09ceed0-5576-4cd0-85fe-3c767d7493d4)

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="641" height="427" alt="image" src="https://github.com/user-attachments/assets/d4522243-cbb5-4d4a-a2cf-a27f2e756ba1" />

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
|       2000-66           |        2004-02           |
|       2001-66           |        2005-00           |
|       2002-33           |        2006-00           |
|       2003-33           |        2007-00           |
#### Manual Calculations

![IMG-20251024-WA0015 1](https://github.com/user-attachments/assets/9a5a5db2-4d2f-4091-b581-2c721541e668)

---
## OUTPUT FROM MASM SOFTWARE

<img width="642" height="432" alt="image" src="https://github.com/user-attachments/assets/300366a7-b07d-466c-8207-c488da2168a9" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

