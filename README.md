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

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|      1200 : 12          |        1204 : 24         |
|      1201 : 34          |        1205 : 68         |  
|      1202 : 12          |        1206 : 00         |
|      1203 : 34          |                          | 


#### Manual Calculations

![WhatsApp Image 2026-02-09 at 08 19 42](https://github.com/user-attachments/assets/3a6f559e-04a5-462b-a5e2-5ca9ed59c2a3)


---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="540" height="300" alt="debug_000" src="https://github.com/user-attachments/assets/3bbca00c-6660-43b1-be90-9012327f1f2c" />

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
|      1200 : 12          |        1204 : 00         |
|      1201 : 34          |        1205 : 00         |  
|      1202 : 12          |                          |
|      1203 : 34          |                          |  


#### Manual Calculations

![sub](https://github.com/user-attachments/assets/ea1b1a4b-0550-4e83-88b5-402f51ca0c83)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="540" height="300" alt="debug_001" src="https://github.com/user-attachments/assets/ff730153-68b5-4301-a2f2-b78d75d9fa5f" />

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
|      1200 : 12          |        1204 : 90         |
|      1201 : 34          |        1205 : 5A         |  
|      1202 : 12          |        1206 : 4B         |
|      1203 : 34          |        1207 : 01         | 


#### Manual Calculations


![mul](https://github.com/user-attachments/assets/c7c35a76-5153-43cd-bfec-d4bbf53f6f32)


---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="540" height="300" alt="debug_002" src="https://github.com/user-attachments/assets/7e96f009-f4ea-450c-b76f-f6841372e3e4" />

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
|      1200 : 12          |        1204 : 01         |
|      1201 : 34          |        1205 : 00         |  
|      1202 : 12          |        1206 : 00         |
|      1203 : 34          |        1207 : 00         |  


#### Manual Calculations

![div](https://github.com/user-attachments/assets/f827826f-6f5a-42e8-b07c-7061d23c641a)

---
## OUTPUT FROM MASM SOFTWARE


<img width="540" height="300" alt="debug_003" src="https://github.com/user-attachments/assets/a17eb401-a191-46d1-bec8-86c19aa0b160" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

