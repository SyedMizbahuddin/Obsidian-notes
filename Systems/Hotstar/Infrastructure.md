 [Source](https://youtu.be/9b7HNzBB3OQ)
 
- Auto Scaling: cannot keep up with the extreme growth rate. 1M request/sec.
   
   You can configure for 60% usage of the CPU start auto scale but even before new server starts up in 90 sec the existing server will get bloated and go down.
   
   Challenges in Auto scaling:
	1. Going from 200 to 800 servers take huge time.
	2. Searching for 600 servers of same configuration in 3 availability zones is not easy
	3. It performs in steps 10 servers in each zone then next 10 set. Huge time.
	4. If a zone does not have configured machine then exponential backoff makes it worse.
   
   Proactive Scaling: 
	1. With analysis identify how many servers are needed, 2M Request/sec need 800 server etc.
	2. Proactively before match procure the servers with any possible configuration using priority order.
   
- Project HULK: This is for 
1. s
2. s
3. s
4. 
   
   