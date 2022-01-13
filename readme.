insert into employee (eid, ename,age,joining_date,salary,manager_id) values
(107, 'rishabh',23,current_date,450000,101), (108, 'shiva',24, current_date, 500000,102),(109,'naveen',23,current_date,500000,102),(110,'rohit',24,current_date,600000,100),(111,'shyam',23,current_date,500000,101),(112,'akash',22,current_date,450000,102);

alter table employee add project_id varchar(10) 
select * from employee;

--qn1 

SELECT eid as EmpID, ename as "Employee Name" FROM employee WHERE manager_id = 101;

--qn 2

select count(*) from employee where project_id='p1';

--qn 3

--max salary
SELECT eid,salary FROM  employee where salary
= (select max(salary) from employee);
--min salary
SELECT eid,salary FROM  employee where salary
= (select min(salary) from employee);
--average salary 
SELECT AVG(salary) AS "Avg Salary"
FROM employee

-- qn 4
SELECT eid,salary FROM  employee WHERE salary BETWEEN (SELECT 10000) AND 15000;

--qn 5
select eid,salary+5000 as new_salary from employee;

--qn 6

 select eid from EmployeeDetails where eid in (select eid from EmployeeSalary);

-- qn 7
SELECT 
    UPPER(ename) as "ename" and LOWER(city) as "city"
	FROM employee 

--qn 8 
select project_id,count(eid) from Employee group by(project_id) order by count(eid) desc;

-- qn 9
select * from Employee where mod(eid,2)<>0;

-- qn 10
 SELECT MAX(salary) FROM employee WHERE salary != (SELECT MAX(salary) 
 FROM employee WHERE salary NOT IN(SELECT MAX(salary) FROM employee)) 
 AND salary != (SELECT MAX(salary) FROM employee);
