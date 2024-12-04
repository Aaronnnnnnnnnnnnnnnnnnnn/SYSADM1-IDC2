![image](https://github.com/user-attachments/assets/b19ae85b-583d-4edc-bdb1-56ac259f5f3f)


# SYSADM1 -- Capacity Management & Planning

**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![image](https://github.com/user-attachments/assets/18f414e6-c79e-44d4-bb69-59851db1ef59)

Identified Problems: \
One ISP
	- The proposed network relies on a single ISP, creating a single point of failure for internet connectivity.
Lack of Redundancy in Core Switch and Edge Routers
	- If either the core switch or edge router fails, the whole network cannot connect to the internet anymore.
Limited Scalability
	- Having only one core switch and three layer 2 switches connecting the servers and PCs will limit the scalability of devices. It will be harder to add more devices in the future.
Potential Bottleneck
	- Having only one core switch and single ports connecting the servers and PCs to layer 2 switches will increase the likelihood of congestion if there is a surge in traffic.
Shared VLAN
	- Some servers share their VLANS. This is fine if they are meant to be connected to each other but without vlan segmentation and security measures (like ACLs), they can access each other with no problem.
Security Risk
	- No mention of security measures (like ACLs and firewalls), leaving the network vulnerable to attacks like DDOS and unauthorized access.

![image](https://github.com/user-attachments/assets/f345952d-d030-4c94-94e5-0cd338b3d3fe)



  ------------------------------------------------------------------------------
  Criteria          Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                           4pts
  ----------------- ------------------ ------------------- ---------------------
  **Network         Accurately         Identifies key      Identifies some basic
  Analysis**        identifies         network components  network components
                    potential          and some potential  but lacks a
                    bottlenecks,       bottlenecks.        comprehensive
                    security risks,                        analysis.
                    and capacity                           
                    limitations.                           

  **Scalability     Proposes multiple  Proposes some       Proposes limited
  Planning**        relevant solutions relevant            scalability
                    and provides       scalability         strategies.
                    detailed           strategies but      
                    explanations,      lacks detail.       
                    including                              
                    potential                              
                    drawbacks and                          
                    benefits.                              

  **Evaluation of   Proposes           Provides a basic    Does not evaluate the
  Solutions**       comprehensive      evaluation of the   proposed solutions or
                    scalability        proposed solutions, provides a
                    strategies,        but lacks depth.    superficial
                    including specific                     evaluation.
                    recommendations                        
                    for hardware                           
                    upgrades, software                     
                    configurations,                        
                    and network                            
                    optimizations.                         

  **Proposed        Provides a         Provides a basic    Does not provide a
  Design**          detailed and       design but lacks    clear and detailed
                    well-justified     specific details    design.
                    design, including  and justifications. 
                    network diagrams,                      
                    configuration                          
                    details, and                           
                    implementation                         
                    plans.                                 

  **Evaluation and  Provides a         Provides a basic    Does not evaluate the
  Justification**   thorough           evaluation of the   proposed solutions or
                    evaluation of the  proposed solutions, provides a
                    proposed           but lacks depth.    superficial
                    solutions,                             evaluation
                    considering                            
                    factors like cost,                     
                    complexity, and                        
                    potential impact.                      

  Score:                                                   /50
  ------------------------------------------------------------------------------
