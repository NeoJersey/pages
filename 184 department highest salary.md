- https://leetcode-cn.com/problems/department-highest-salary/
- ![image.png](../assets/image_1647868944496_0.png)
- 用group by departmentId 来找出每个部门的最高工资
- 用(deparment, salary) in来成对匹配找出各部门拿最高工资的人
- ```
  with max_salary as(
  select d.name, d.id, max(e.salary) Salary
  from employee e left join department d on e.departmentId = d.id
  group by d.id
  )
  
  select m.name Department, e.name Employee, m.salary Salary
  from max_salary m left join employee e 
  on (m.id, m.salary) = (e.departmentId, e.salary)
  
  #这样比不join的快
  ```