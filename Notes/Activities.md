# Question 01

![[Pasted image 20261108192505.png]]

Here, $R$ follows the 1NF ([[1st Normal Form]])

1. $FD_{1}$ --> Fully dependency in 2NF
2. $FD_{2}$ --> Part of the key - Partial dependency (violates 2NF)
3. $FD_{3}$ --> ""
4. $FD_{4}$ --> Left side is nonprime (violates BCNF)

---

## Steps

**Need to follow the steps in order**: 1NF --> 2NF --> 3NF --> BCNF

1. **Step 01:** Convert 1NF --> 2NF (by removing $FD_{2}$ & $FD_{3}$)
	- ![[Pasted image 20261108193635.png|295]]
2. **Step 02:** Convert 2NF --> 3NF (no violations)
3. **Step 03:** Convert 3NF --> BCNF (by removing $FD_{4}$)
	- ![[Pasted image 20261108194212.png|338]]
4. **Step 04:** Bringing all the relations together

---

# Question 02

Here, `COUNTRY_NAME` & `LOT#` are *candidate keys*

![[Pasted image 20261108194909.png]]

1. $FD_{1}$ --> Fully dependency in 2NF
2. $FD_{2}$ --> Fully dependency in 2NF (it's because, `PROPERTY_ID` and `COUNTRY_NAME` & `LOT#` are 2 different super keys)
	- `PROPERTY_ID` is a single super key
	- `COUNTRY_NAME` & `LOT#` together another super key called *candidate keys*
3. $FD_{3}$ --> Partial dependency (violates 2NF)
4. $FD_{4}$ --> Both are nonprime keys (violates 3NF)
5. $FD_{5}$ --> Left side is nonprime (violates BCNF)

---

## Steps

1. **Step 01:** 1NF --> 2NF (removing $FD_{3}$)
	- ![[Pasted image 20261108205047.png|320]]
2. **Step 02:** 2NF --> 3NF (removing $FD_{4}$)
	- ![[Pasted image 20261108205204.png|319]]
3. **Step 03:** 3NF --> BCNF (removing $F_{5}$)
	- ![[Pasted image 20261108205317.png|321]]
4. **Step 04:** Bringing all relations together

---

# Question 03

Consider a relation $R(ProjectNo,ProjectName,EmpNo,EmpName,DeptNo,DeptName,HrsWork)$ with the following set of functional dependencies $F$ over $R$:
```
F = {
      ProjectNo -->  ProjectName   (FD1)
      DeptNo    -->  DeptName      (FD2)
      EmpNo     -->  EmpName, DeptNo, DeptName, HrsWork   (FD3)
}
```
#### a) Find all the keys in relation $R$ using **attribute closure method**
$$
(ProjectNo)^+ = \{ProjectNo, ProjectName\} \\
(DeptNo)^+ = \{DeptNo, DeptName\} \\
(EmpNo)^+ = \{EmpNo, EmpName, DeptNo, DeptName, HrsWork\} \\
(ProjectNo + EmpNo)^+ = \{ProjectNo, ProjectName, EmpNo, EmpName, DeptNo, DeptName, HrsWork\}
$$
1. $FD_{1}$ --> Partial dependency (violates 2NF)
2. $FD_{2}$ --> Both are nonprime keys (violates 3NF)
3. $FD_{3}$ --> Partial dependency (violates 2NF)