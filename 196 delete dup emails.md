- https://leetcode.com/problems/delete-duplicate-emails/
- ![image.png](../assets/image_1647791100678_0.png)
- 用一个相同的表来对比，以获得重复值和筛选出较小的id
- ```
  delete p1 
  from person p1, person p2
  where p1.email = p2.email and p1.id>p2.id
  ```