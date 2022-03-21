- specify rows to skip
- ```
  select * from table limit 5 offset 2 %return row 3~8
  ```
- offset 和 limit的参数都必须是数字，不能是运算
  ```
  offset N-1  % error
  ```
  ```
  declare m int;
  set m=N-1;
  offset m % okay
  ```