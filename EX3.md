# EX 3 SubQueries, Views and Joins 
## Date:

## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql
INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:

![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/e29c0ee1-58e3-4a70-bc42-aab70ce330f0)

### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/37aa96d6-f101-4ff6-94e9-4bee4c5893c1)

### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/154fa3f0-690b-41e5-bb9a-f4843dbf9d24)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/d2fa9319-1c27-4312-90d5-3475e0578465)

### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/2d187552-8518-4deb-a38a-522dde38772e)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/72f14e58-5682-4e6a-be2e-96b365263746)


### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/09939578-f71c-43c1-bb18-e763fab962ae)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/9e2cb9e6-de71-43c7-b2b2-04e48baa097f)

### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:

![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/bb465984-029b-400c-970f-3572691db35d)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/129fa53d-4eca-4bc1-9347-b92f243a8072)

### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/e760c852-e5a7-4f9e-afcf-5f7e8a7dd431)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/4bad4157-a175-4fcf-a14a-59166a727fc3)

## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/29ff6623-08a7-429e-83d7-4cd5096cd511)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/da07ac2d-1dc9-45fc-a651-ed03de0ce3f0)

### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/739aae28-821e-440e-9d82-53e2fe311633)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/b7806f48-bb05-49fb-92c6-9d396fbfee3a)

### Q9) Perform Natural join on both tables

### QUERY:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/ec0ebf05-0d04-4297-badc-d6ef93bbe084)


### OUTPUT:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/95330863-0f2f-43e5-890b-7b06f562681d)

### Q10) Perform Left and right join on both tables

### QUERY:

![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/82395371-b223-4b10-87fe-9d082c124c26)

### OUTPUT:
### Left joint:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/676213b7-1005-42c4-9fe2-9c92918d7e8b)

### Right joint:
![image](https://github.com/kanishka2305/EX-3-SubQueries-Views-and-Joins/assets/113497357/75999852-0abf-4a01-81a1-fbbd73a1fd05)

## Result:
Hence successfully created a manager database and executed views and joins using SQL.
