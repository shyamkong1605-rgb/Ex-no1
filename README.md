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
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
<img width="1329" height="740" alt="WhatsApp Image 2026-05-11 at 9 27 52 AM" src="https://github.com/user-attachments/assets/4646f330-7927-4832-859a-53661938b228" />



#### Manual Calculations

<img width="3818" height="1722" alt="WhatsApp Image 2026-05-11 at 9 27 26 AM" src="https://github.com/user-attachments/assets/22cb4f05-39cf-4f1f-a192-0befdeb5ba40" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="1424" height="1009" alt="WhatsApp Image 2026-05-11 at 9 28 20 AM" src="https://github.com/user-attachments/assets/11d849ee-9a82-425d-a273-02963ce5b6d5" />


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
<img width="2964" height="1886" alt="WhatsApp Image 2026-05-11 at 9 29 47 AM" src="https://github.com/user-attachments/assets/37d99df7-355c-4206-9b6c-768c4c4ce1a5" />


#### Manual Calculations

<img width="1600" height="923" alt="WhatsApp Image 2026-05-11 at 9 28 53 AM" src="https://github.com/user-attachments/assets/8e5b66a4-a83c-41dd-b29d-061d7e15e75b" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1550" height="991" alt="WhatsApp Image 2026-05-11 at 9 30 05 AM" src="https://github.com/user-attachments/assets/3d054c85-7dba-4e9b-be4d-8772d8991a40" />


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
<img width="1600" height="963" alt="WhatsApp Image 2026-05-11 at 9 31 29 AM" src="https://github.com/user-attachments/assets/5ad6a447-fc28-48ce-93f1-2f0c8844c152" />


#### Manual Calculations

<img width="1484" height="968" alt="WhatsApp Image 2026-05-11 at 9 31 09 AM" src="https://github.com/user-attachments/assets/bdf716a3-cff1-41cb-bc87-3207d46a11e8" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="1600" height="990" alt="WhatsApp Image 2026-05-11 at 9 31 47 AM" src="https://github.com/user-attachments/assets/9f895288-2ff8-4a92-ad04-0f37a6e0b1ac" />


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

<img width="1600" height="963" alt="WhatsApp Image 2026-05-11 at 9 32 15 AM" src="https://github.com/user-attachments/assets/23090f38-a9f1-47f4-8925-93178798dc83" />

#### Manual Calculations

<img width="1600" height="900" alt="WhatsApp Image 2026-05-11 at 9 32 27 AM" src="https://github.com/user-attachments/assets/16b1c948-3937-4fd9-a8e3-05a0a6e41453" />


---
## OUTPUT FROM MASM SOFTWARE
<img width="1549" height="1044" alt="WhatsApp Image 2026-05-11 at 9 32 49 AM" src="https://github.com/user-attachments/assets/58a63b2b-5864-4492-8dbc-20d515b9b5b7" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

