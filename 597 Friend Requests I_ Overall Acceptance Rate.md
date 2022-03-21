title:: 597 Friend Requests I: Overall Acceptance Rate

- https://leetcode-cn.com/problems/friend-requests-i-overall-acceptance-rate/
- ![image.png](../assets/image_1647872908826_0.png)
- ```
  select
      round( # round to 2 decimals
          ifnull( # if null, return 0
              (select count(distinct requester_id, accepter_id) from requestAccepted)
              /
              (select count(distinct sender_id, send_to_id) from friendRequest)
              , 0
          )
          , 2
          ) as accept_rate
  ```