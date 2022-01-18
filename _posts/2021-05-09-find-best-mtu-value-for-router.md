---
title: How to find the best MTU value for Router?
layout: post-right-sidebar
categories:
- Windows
- Network
image: assets/images/post/MTU.png
featured: false
---

MTU (Maximum Transmission Unit) size is the maximum packet size that is permitted on your network. When the MTU value is more than the permitted there will be packet loss.
So it is recommended to maintain the ideal MTU value in your router configuration to increase the network perfomance.

You can set the optimal MTU value in the Router configuration page

**But how to find the optimal MTU value?**

To find the optimal MTU value in Windows

1. Open Command prompt

2. Enter the following command
 
    ```
    ping www.google.com -f -l 1500
    ```
![]({{ 'assets/images/post/MTU02.png' | relative_url }})

3. If you are getting the message as "Packet needs to be fragmented but DF set" and Loss of 100%. 

4. Then, reduce the MTU value by 10 as 1490 and re-execute the command.

5. Repeat the steps until you get Loss = 0%.

	![]({{ 'assets/images/post/MTU03.png' | relative_url }})

6. From the current MTU value, increase the count by 1 and find out the maximum value with 0 % Loss.

Add 28 to the maximum value you have found out and update it in the router configuration.

![]({{ 'assets/images/post/MTU-01.png' | relative_url }})
