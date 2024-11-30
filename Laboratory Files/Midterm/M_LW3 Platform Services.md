+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 29aa5f14f95a4a3fbf17c94ce1fc9a5f |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Aaron Joshua G. Sese       | DATE PERFORMED:        | /50      |
|                                  | 10/17/2024             |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 10/17/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Platform Services

# Requirement: 

-   A virtual machine running Windows Server

    **Objective/s:**

    To analyze IIS logs in the Event Viewer to identify critical web
    service metrics, understand common error codes, and learn how to
    monitor the health of web applications.

**Instructions**

**Part 1: Opening Event Viewer and Loading Logs**

1.  Access the event viewer in the server.

2.  From the event viewer, explore the windows log and list down its
    major categories

-   The Windows Log has 5 major categories: Application, Security,
    Setup, System and Forwarding Events

**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

![](vertopal_29aa5f14f95a4a3fbf17c94ce1fc9a5f/media/image2.png){width="5.938810148731409in"
height="5.872187226596675in"}

2.  **Identify Critical Events** or recurring events.

> ![](vertopal_29aa5f14f95a4a3fbf17c94ce1fc9a5f/media/image3.png){width="6.209199475065617in"
> height="1.8440069991251093in"}

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

        -   **Event ID**

        -   **Source**

        -   **Timestamp**

        -   **Description**

  ------------------------------------------------------------------------
  **Event   **Source**         **Timestamp**      **Description**
  ID**                                            
  --------- ------------------ ------------------ ------------------------
  7023      Service Control    10/17/2024 8:34:13 The Windows Time service
            Manager            AM                 terminated with the
                                                  following error: An
                                                  attempt was made to
                                                  logon, but the network
                                                  logon service was not
                                                  started.

  7023      Service Control    10/17/2024 8       The Windows Time service
            Manager            :34:50 AM          terminated with the
                                                  following error: An
                                                  attempt was made to
                                                  logon, but the network
                                                  logon service was not
                                                  started.

  7023      Service Control    10/17/2024         The IP Helper service
            Manager            11:03:14 PM        terminated with the
                                                  following error: The
                                                  service cannot be
                                                  started, either because
                                                  it is disabled or
                                                  because it has no
                                                  enabled devices
                                                  associated with it.

  46        volmgr             11/17/2024         Crash dump
                               11:03:03 PM        initialization failed!

  46        Time-Service       10/17/2024 8:34:13 The time service
                               AM                 encountered an error and
                                                  was forced to shut down.
                                                  The error was:
                                                  0x80070700. An attempt
                                                  was made to logon, but
                                                  the network logon
                                                  service was not started.

  46        Time-Service       10/17/2024 8:34:50 The time service
                               AM                 encountered an error and
                                                  was forced to shut down.
                                                  The error was:
                                                  0x80070700. An attempt
                                                  was made to logon, but
                                                  the network logon
                                                  service was not started.
  ------------------------------------------------------------------------

**There are no CRITICAL errors logged in the Event Viewer.**

**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

2.  Is there a specific time or pattern to these errors?

3.  Draft a Troubleshooting Report:

    -   Based on the events found, create a short report with the
        following sections:

**Report Structure**

**1.** Overview

-   A brief summary of the issue and scope of your analysis.

**2.** Key Findings

-   List the critical events you found. Example:

    -   **Event ID 503**: Application pool stopped at 10:05 AM.

    -   **Event ID 404**: Page not found error at 11:15 AM.

**3.** Root Causes and Solutions

-   Describe the likely cause of each error and how you would fix it.

Report:

Overview

\- This report analyzes several error events logged on October 17, 2024.
While these events may not seem directly related to web servers, some
can impact critical functions like network communication, time
synchronization, and system stability, which are essential for smooth
web server operations.

Key Findings

\- **Event ID 7023:** The Windows Time service failed to start at 8:34
AM due to a missing Network Logon service.

\- **Event ID 7023**: The IP Helper service terminated at 11:03 PM
because the service was either disabled or lacked necessary devices.

\- **Event ID 46**: Crash dump initialization failed at 11:03 PM**,**
preventing the system from logging memory data during failures.

\- **Event ID 46**: The time service encountered an error (0x80070700)
at 8:34 AM due to the Network Logon service not being started.

Root Causes and Solutions

Cause:

\- Windows Time Service Failures happens because of time discrepancies.

Solution:

\- Ensure Network Logon service is running, as it is required by the
Windows Time service.

\- Synchronize the time of the server and client.

Cause:

\- IP Helper Service Termination is enabled but IPv4 is only being used.

Solution:

\- Disable the IP Helper Service to prevent unnecessary errors.

Cause:

\- Crash Dump Initialization Failure might happen because of
insufficient disk space

Solution:

\- Ensure there is sufficient disk space on the system drive for crash
dumps.

**Part 4: Reflection Questions**

1.  What are the most common causes of **Event ID 7023**?

-   This event happens when a Windows Service unexpectedly stops. Common
    causes include missing or disabled dependencies, misconfigured
    services, corrupted files or insufficient system resources.

2.  How would you **monitor login attempts** to detect potential
    security threats?

-   I can monitor login attempts using the Event Viewer by going to
    Windows Logs then Security. Successful and failed logins would be
    recorded in the logs. I can then look for signs like many failed
    logins in a row to detect any potential security threats.

3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

-   Checking logs in Event Viewer help administrators spot problems
    early like services failing or several failed login attempts. It
    also helps keep systems running smoothly by showing errors or any
    information important about the system. Reviewing logs regularly
    makes it easier to fix issues fast and keeps the system safe.

Grading Rubric

  ---------------------------------------------------------------------------------------------------------------------------------------
  **Criteria**        **Excellent**     **Good**          **Needs                           **Poor**                         **Points**
                                                          Improvement**                                                      
  ------------------- ----------------- ----------------- --------------- ----------------- ------------- ------------------ ------------
  **Log Analysis**    Identifies all    Identifies most   Identifies some                   Fails to                         /10
                      key events (503,  key events with   events, but                       identify key                     
                      404, 500, etc.)   minor errors in   with incomplete                   events or                        
                      with accurate     details.          or incorrect                      provides                         
                      event details.                      details.                          incorrect                        
                                                                                            details.                         

  **Troubleshooting   Proposes logical, Solutions are     Solutions are                     Solutions are                    /10
  Solutions**         effective         mostly correct    somewhat vague                    unclear or                       
                      solutions to all  but miss some key or incomplete.                    incorrect.                       
                      identified        points.                                                                              
                      issues.                                                                                                

  **Report Structure  Well-organized    Report is mostly  Report is                         Report is                        /10
  & Clarity**         report with all   organized with    disorganized or                   unclear or                       
                      sections clearly  minor formatting  missing                           incomplete.                      
                      completed.        issues.           sections.                                                          

  **Recommendations   Provides          Recommendations                   Recommendations                 Fails to provide   /10
  for Monitoring**    thoughtful,       are relevant but                  are vague or                    relevant           
                      proactive         lack depth.                       incomplete.                     recommendations.   
                      recommendations                                                                                        
                      to prevent future                                                                                      
                      issues.                                                                                                

  **Participation &   Actively engaged  Participated but                  Minimal                         Did not            /10
  Effort**            in the activity,  required some                     participation,                  participate        
                      followed          guidance.                         needed                          meaningfully.      
                      instructions                                        significant help.                                  
                      thoroughly.                                                                                            

  **Score**                                                                                                                  **/50**
  ---------------------------------------------------------------------------------------------------------------------------------------
