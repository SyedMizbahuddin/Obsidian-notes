 [Source](https://youtu.be/9b7HNzBB3OQ)
 
- **Auto Scaling**: cannot keep up with the extreme growth rate. 1M request/sec.
   
   You can configure for 60% usage of the CPU start auto scale but even before new server starts up in 90 sec the existing server will get bloated and go down.
   
   Challenges in Auto scaling:
	1. Going from 200 to 800 servers take huge time.
	2. Searching for 600 servers of same configuration in 3 availability zones is not easy
	3. It performs in steps 10 servers in each zone then next 10 set. Huge time.
	4. If a zone does not have configured machine then exponential backoff makes it worse.
   
   Proactive Scaling: 
	1. With analysis identify how many servers are needed, 2M Request/sec need 800 server etc.
	2. Proactively before match procure the servers with any possible configuration using priority order.
   
- **Project HULK, Chaos Engineering**: This is for stress testing replaying the user journey.   Breaking the systems purposefully
  
- **User Journey**: The best way to improve scale is by understanding the user journey.
  Before the match the user lands on the home page, and right after the match user lands on the home page, so it is important to scale both home and Live Streaming.
  
- **Feature flags**: This is very very useful, this allows to turn off any feature any time to be able to save compute when we s crunch of resources. This can be turned off based on geography, audience type, OS, device etc.
  
- **Panic mode**: During failure, we need our P0 services (streaming, ads, payment) to up and running at the cost of P1, P2 services, during breakage recommendation systems, personalization systems, profile etc. are turned off. can use Static Response taking snapshot of the response and showing same to everyone, ex: same homepage for everyone
- **DB scaling**:  Scaling up DB more replicas addition takes huge time 45 min, hence this needs to be scaled up before hand using back of the envelope cal

   