source: https://liip.slack.com/archives/C02K3G9US/p1647252397862119


Oh gosh... I had a weird Bug and couldn't find it, but now I figure it out: Summer time (Daylight saving) is coming up on Sunday, 27 March and I made wrong assumptions...
I always make the same mistakes...
## Question
What are your top 3 causes of bugs you write? And how do you avoid it?
((See thread for mine)) (edited) 

Here are my top 3 causes of bugs I usually write:
* *Problem*: Access non existing keys in an object `obj.test`  *Solution*: `obj?.test` or `obj && obj.test` (TS for the win)
* *Problem*: Date & Time stuff. *Solution*: I try to work with timestamps (int) and if not possible I try to work with UTC-Time for calculation. Most of the time I realise `moment.js` would have saved me but I usually don't take it because it's just a huge dependency in terms of file-size in the browser.
* *Problem*: recursion. *Solution*: try whenever possible to do it in loops.
