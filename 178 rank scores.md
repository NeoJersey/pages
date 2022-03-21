- https://leetcode.com/problems/rank-scores/
- ![image.png](../assets/image_1647882082636_0.png)
- ```
  select score,
  dense_rank() over(order by score desc) as "rank"
  from scores
  ```