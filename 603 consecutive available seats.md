- ![image.png](../assets/image_1647873538574_0.png)
- https://leetcode-cn.com/problems/consecutive-available-seats/
- 用abs(a.seat_id - b.seat_id)=1来获得连续座位
- ```
  select distinct a.seat_id
  from cinema a,cinema b
  where abs(a.seat_id - b.seat_id) = 1 and a.free = 1 and b.free = 1
  order by seat_id
  ```
-