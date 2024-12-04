![image](https://github.com/user-attachments/assets/2105a9a4-4d9a-4578-a5eb-2133d5a07e37)


# SYSADM1 -- Capacity Management & Planning

**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

![image](https://github.com/user-attachments/assets/7939aca9-7682-44f0-9ed8-e55635f1ce7f)


**Identified Problems:**

-   One ISP

    \- The proposed network relies on a single ISP, creating a single
    point of failure for internet connectivity.

-   Lack of Redundancy in Core Switch and Edge Routers

    \- If either the core switch or edge router fails, the whole network
    cannot connect to the internet anymore.

-   Limited Scalability

    \- Having only one core switch and three layer 2 switches connecting
    the servers and PCs will limit the scalability of devices. It will
    be harder to add more devices in the future.

-   Potential Bottleneck

    \- Having only one core switch and single ports connecting the
    servers and PCs to layer 2 switches will increase the likelihood of
    congestion if there is a surge in traffic.

-   Shared VLAN

    \- Some servers share their VLANS. This is fine if they are meant to
    be connected to each other but without vlan segmentation and
    security measures (like ACLs), they can access each other with no
    problem.

-   Security Risk

    \- No mention of security measures (like ACLs and firewalls),
    leaving the network vulnerable to attacks like DDOS and unauthorized
    access.

**Solutions:**

1.  **Transitioned to a 3-Tier Architecture**

-   **Benefits**

    \- Core Layer will handle traffic faster, which will be the backbone
    of the network.

    \- Distribution Layer improves scalability, allowing more access
    switches (layer 2 switches) to be added without overloading the
    core.

    \- Enhances redundancy with dual port connections between layers.

-   **Drawbacks**

    \- Increased hardware costs for distribution switches and additional
    ports.

    \- Additional configuration and maintenance complexity.

2.  **Dual ISP**

-   **Benefits**

    \- Improves uptime with failover capability if one ISP goes down.

    \- Enables load balancing to split traffic, enhancing performance.

-   **Drawbacks**

    \- Higher recurring costs due to having a second ISP.

3.  **Redundant Edge Routers and Core Switches**

-   **Benefits**

    \- Prevents single points of failure.

    \- Maintains network availability if a router or switch fails.

-   **Drawbacks**

    \- Higher initial cost for additional hardware.

4.  **Improved Access Layer**

-   **Benefits**

    \- Dedicated VLANs for server-PC groups improve traffic segmentation
    and performance.

-   **Drawbacks**

    \- Higher initial cost for additional hardware.

    \- Additional configuration and maintenance complexity.

5.  **Implemented Firewalls in Edge Routers**

-   **Benefits**

    \- Firewalls on edge routers provide a first line of defense against
    external threats, such as DDoS attacks, unauthorized access, and
    malware.

    \- Enhances traffic filtering to block suspicious or malicious
    packets before they reach internal systems.

-   **Drawbacks**

    \- Adds processing overhead to routers, which could impact
    performance if not optimized.

    \- Requires regular updates and monitoring.

    **The Solution:**

![](vertopal_16db6510f2c04d86b7127b5d1b89e03e/media/image3.png){width="7.0256944444444445in"
height="3.361111111111111in"}

Cost

\- The 3-tier architecture provides higher initial costs for additional
routers, switches, and ports.

\- Dual ISPs add recurring costs.

Complexity

\- Configuration and maintenance are more complex due to the added
redundancy, VLANs, and security features.

\- Firewalls require ongoing monitoring and updates to ensure
effectiveness.

Impact

\- Eliminates single points of failure, ensuring network availability
even during high traffic surges.

\- Scalable, supports future growth, as access switches and VLANs can
easily be added without impacting the existing network.

\- Provides security against external and internal threats through
firewall.

\- Enhances performance by segmenting traffic (VLANs) and balancing
loads efficiently (Dual ISP load balancing).

  ----------------- ------------------ ------------------- ---------------------
  Criteria          Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                           4pts

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
  ----------------- ------------------ ------------------- ---------------------
