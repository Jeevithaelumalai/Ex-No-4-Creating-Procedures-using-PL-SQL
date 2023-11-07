# Ex-No-4-Creating-Procedures-using-PL-SQ
## DATE:24/8/2023
## AIM: To create a procedure using PL/SQL.
### Steps:
1.Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2.Create a procedure named as insert_employee data.
3.Inside the procdure block, write the query for inserting the values into the employee table.
4.End the procedure.
5.Call the insert_employee data procedure to insert the values into the employee table.
6.Display the employee table
### Program:
```
CREATE TABLE employee (
  empid INT PRIMARY KEY,
  empname VARCHAR(10),
  dept VARCHAR(10),
  salary DECIMAL(10, 2)
);
```
```
DELIMITER //

CREATE PROCEDURE insert_employee_data(
  IN p_empid INT,
  IN p_empname VARCHAR(10),
  IN p_dept VARCHAR(10),
  IN p_salary DECIMAL(10, 2)
)
BEGIN
  INSERT INTO employee (empid, empname, dept, salary)
  VALUES (p_empid, p_empname, p_dept, p_salary);
END //

DELIMITER ;
```
```
CALL insert_employee_data(1, 'John', 'HR', 50000.00);
CALL insert_employee_data(2, 'jeevita', 'IT', 60000.00);
SELECT * FROM employee;
```
### Output:
![image](https://github.com/Jeevithaelumalai/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/118708245/cfcbd780-5025-496b-8370-c90907ec97e4)

### Result:
The procedures has been successfully created using PL\SQL.
