---
tags:
  - PROGRAMING
Year: "2024"
Curriculum: "[[SE-Computer-Engg-2019-Patt.pdf]]"
Semester: SE SEM 3
Course: Computer
Lab: "[[Data Structures Laboratory -]]"
Major: "[[Fundamentals of Data Structures -]]"
github_repo: https://github.com/iceking-1912/school-stuff-meme/tree/Master/DSl/GRP-AB
lab_grp: AB
---
## 4. Bank Account Transaction Log:

- a) Withdraw function (ensures balance does not go negative).
- b) Deposit function.
- _Input format_: D 300, D 300, W 200, D 100.  
    _Output_: Net amount in the bank account.
 - [x] [[SEM-TODO's#^48ade8]] ✅ 2024-08-31
### GitHub link-
[school-stuff-meme/DSl at Master](https://github.com/iceking-1912/school-stuff-meme/tree/Master/DSl/GRP-AB)

## ExcaliDraw link-
[[Bank_Account_Transaction_Log.excalidraw]]

---
###  Base Code

```py

```
---
### A) Transpose 

```py
#transpose of matrix
print("Transpose of Mat1 is:")
mat4 = []
for i in range(len(mat1[0])):
    row = []
    for j in range(len(mat1)):
        row.append(mat1[j][i])
    mat4.append(row)
for row in mat4:
    print(row)
```
---
### B) Fast Transpose.

```py
fmat= []
for i in range(len(mat1[0])):
    row = []
    for j in range(len(mat1)):
        if (mat1[i][j] > 0):
           row.append(mat1[j][i])
        else:
            row.append(0)
    fmat.append(row) 
for row in fmat:
    print(row)

```
---
### C) Addition

```py
 for row in mat2:
     print(row)
 print("Addition of Mat1 and Mat2 is:")
 mat3 = []
 for i in range(len(mat1)):
     row = []
     for j in range(len(mat1[i])):
         sum = mat1[i][j] + mat2[i][j]
         row.append(sum)
     mat3.append(row)
 for row in mat3:
     print(row)
```
---

# Output 
```
Matrix 1 is:
[0, 0, 3]
[1, 0, 0]
[0, 2, 0]
Matrix 2 is:
[9, 8, 7]
[6, 5, 4]
[3, 2, 1]
Addition of Mat1 and Mat2 is:
[9, 8, 10]
[7, 5, 4]
[3, 4, 1]
Transpose of Mat1 is:
[0, 1, 0]
[0, 0, 2]
[3, 0, 0]
```

---
