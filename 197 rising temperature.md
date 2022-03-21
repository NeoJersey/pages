- https://leetcode.com/problems/rising-temperature/
- [[datediff]]
- ![image.png](../assets/image_1647791498037_0.png)
- join 同一个表，用datediff(d1, d2)=1 来找到昨日
- ```
  select w1.id
  from weather w1 left join weather w2
  on datediff(w1.recordDate, w2.recordDate)=1 # w2.recordDate比w1.recordDate小一天
  where w1.temperature>w2.temperature
  ```