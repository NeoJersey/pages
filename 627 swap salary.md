- [[if]] [[case]]
- https://leetcode.com/problems/swap-salary/
- ![image.png](../assets/image_1647789549465_0.png)
- case:
  ```
  UPDATE Salary
  SET sex = CASE sex
  	WHEN "m" THEN "f"
      ELSE "m"
  END
  
  # or
  CASE 
  	WHEN "m" THEN "f"
      ELSE "m"
  END
  ```
- if:
  ```
  UPDATE Salary
  SET sex = IF(sex="m", "f", "m")
  sql