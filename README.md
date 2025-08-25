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
|           1200h         |        1204h             |
|           1201h         |        1205h             |
|           1202h         |        1206h             |  
|           1203h         |        1207h             |

#### Manual Calculations

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/8e5357f1-33f0-4008-9659-a0040020e337" />


## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (15)" src="https://github.com/user-attachments/assets/d25339f0-a065-49ee-b685-1e693b1fdbb0" />


<img width="640" height="480" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/dbf0c214-8104-435c-ab69-bcf51fba20e6" />

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

<img width="640" height="480" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/3160be85-2876-44a8-9b9b-6da864dcf80d" />



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|           1200h         |        1204h             |
|           1201h         |        1205h             |
|           1202h         |        1206h             |
|           1203h         |        1207h             |
#### Manual Calculations

<img width="640" height="480" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/b67e0aa0-c0b5-4fca-b53c-37df1a5eb5fd" />


<img width="720" height="1280" alt="image" src="https://github.com/user-attachments/assets/82078e76-405c-4b3a-afae-dc71f6fed1d6" />




## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/abdab84b-a772-4e93-b44a-e4f719ab5132" />


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
|    1200                 |        1204              | 
|    1201                 |        1205              | 
|    1202                 |        1206              |
|    1203                 |        1207              |

#### Manual Calculations

<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/9c8b1fa8-6273-4185-a281-e603133f6bd9" />


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="640" height="480" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/4445fc6a-ae89-46c5-a88e-493f3110a196" />



<img width="640" height="480" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/67bb03c2-235b-4d98-960b-503f6e1e8b7d" />


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
|            1200h        |       1204h              |
|            1201h        |       1205h              |
|            1202h        |       1206h              | 
|            1203h        |       1207h              |

#### Manual Calculations


<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/f42f02d9-12a2-4eef-88c7-cdd26a2447dc" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/a7b2ee56-befe-4fc5-96c1-75969915ead3" />



<img width="640" height="480" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/fb3977ba-0f45-43f7-b7ae-fd5ac2730799" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
