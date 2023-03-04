---
layout: post
category: Network Programming
---

Connections are persistent in HTTP/1.1 spec by default. You ask why?

Cause after initial load, browsers for sure ask for images, scripts and styles from the page loaded.

While the convention is to release any resources and memory, immediately after the application is done with them,

It gets interesting when the connection is kept open, you ask how? This is when the IP of TCP/IP kicks in.

Internet protocol (IP) uses datagram packets to find any latencies and congestion in routing, and works around to avoid them. Thus improving the over all quality of the connection.

But in the conventional practice, It takes multiple round-trip each time to establish a socket connection, and a few more for TCP and then HTTP, adding to the latency.

In summary: When you know there will be more requests to follow, it is better to keep the connection alive.

But when and how do you close the connection? That's still mysterious.
