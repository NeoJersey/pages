- https://towardsdatascience.com/a-guide-to-advanced-sql-window-functions-f63f2642cbf9
- An easy way to perform calculation across a set of table rows. One major advantage is to work with both aggregate and non-aggregate values all at once.
- difference from `group by`
  left is `group by`, right is window function
  ![image.png](../assets/image_1647875012082_0.png)
- **Window functions are allowed in select and order by, but not in from, where, group by, or having**
- ![image.png](../assets/image_1647877828267_0.png)
- lag(): values from previous rows. lead(): from following rows
- 注意⚠️：给window 出的column重命名时需要加引号，并且不要重命名为"rank",会出bug
-