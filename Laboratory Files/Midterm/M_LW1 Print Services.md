+----------------------------------+------------------------+----------+
| ![](.                            |                        |          |
| /image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Aaron Joshua G. Sese       | DATE PERFORMED:        | /50      |
|                                  | 3/10/2024              |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 3/10/2024              |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

> ![](./image2.png){width="5.6570395888014in"
> height="2.7295472440944883in"}

2.  Connect one client to the recently created domain

> ![](./image3.png){width="4.198502843394576in"
> height="1.8231714785651794in"}

3.  Install Print Services Role:

> ![](./image4.png){width="5.827725284339458in"
> height="4.063685476815398in"}

4.  Search the internet for any printer installer and convert it to iso

> ![](./image5.png){width="6.396725721784777in"
> height="0.27087160979877517in"}

5.  Install and deploy it as network printer

> ![](./image6.png){width="6.1831649168853895in"
> height="5.082062554680665in"}
>
> ![](./image7.png){width="4.761081583552056in"
> height="4.1047397200349955in"}

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

    -   Review logs for print jobs, errors, and warnings.

> ![](./image8.png){width="4.188083989501313in"
> height="0.9480489938757656in"}
>
> ![](./image9.png){width="4.063066491688539in"
> height="4.5006277340332455in"}
>
> ![](./image10.png){width="4.042230971128609in"
> height="4.386029090113736in"}

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

    -   In the left pane, expand Data Collector Sets \> System.

    -   Right-click System Performance and select Start.

    -   Monitor performance metrics related to print services.

> ![](./image11.png){width="6.087398293963255in"
> height="1.9906321084864391in"}

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

> ![](./image12.png){width="6.803032589676291in"
> height="0.7605227471566054in"}

Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

**PaperCut**

Features

-   Print Security and Data loss prevention

-   Easier Setup for Printers

-   On-device MFD Embedded Software

-   3D Printing Option

Pricing

-   Users: 0-5 25 50 75 100

-   Price: FREE! \$482 \$582 \$670 \$753

Compatibility

-   Microsoft Windows (64-bit) Server 2022 / 2019 / 2016 / 2012 /
    Windows 11 / Windows 10

**Pharos**

Features

-   Data Privacy and Document Storage

-   Cloud Features

-   Integration APIs

-   Delegate Print

Pricing

-   Request A Demo

Compatibility

-   Windows Server 2022, Windows Server 2019, Windows Server 2016,
    Windows Server 2012 R2

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

    -   Follow the installation instructions provided by the tool\'s
        documentation.

    -   Configure it to monitor your print services.

![](./image13.png){width="7.027083333333334in"
height="4.935416666666667in"}

![](./image14.png){width="7.027083333333334in"
height="2.8833333333333333in"}

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

    -   Analyze the collected data (e.g., print volume, errors, user
        activity).

Printer Description:

![](./image15.png){width="7.027083333333334in"
height="0.9208333333333333in"}

The server only has one printer available which is the EPSON L6170
Series. The cost to print is \$0.30 which is charged to users.

![](./image16.png){width="6.313381452318461in"
height="6.417562335958006in"}

![](./image17.png){width="6.417562335958006in"
height="6.396725721784777in"}

![](./image18.png){width="6.230036089238845in"
height="6.3029625984251965in"}

![](./image19.png){width="7.027083333333334in"
height="5.1715277777777775in"}

JOB LOG:

![](./image20.png){width="7.027083333333334in"
height="3.3256944444444443in"}

Administrator Printer a total of 22 pages and is charged \$6.60. In the
Job Log, attributes of the printed document is also showed.

![](./image21.png){width="5.792474846894138in"
height="4.51104658792651in"}

Rubric

  --------------------------------------------------------------------------------------------------------------
  **Criteria**   **1                  **2 (Needs       **3                **4        **5             **Score**
                 (Unsatisfactory)**   Improvement)**   (Satisfactory)**   (Good)**   (Excellent)**   
  -------------- -------------------- ---------------- ------------------ ---------- --------------- -----------

  --------------------------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 1: Setting Up Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Domain         No domain Domain     Domain      Domain       Domain           
  Installation**   created   created    created     configured   configured and   
                             with       correctly   well         documented       
                             errors                              thoroughly       
  ---------------- --------- ---------- ----------- ------------ ---------------- --

  ----------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Client       Client not  Connection   Client      Client      Client        
  Connection**   connected   attempt      connected   connected   connected and 
                             failed       but with    correctly   documented    
                                          issues                  well          
  -------------- ----------- ------------ ----------- ----------- ------------- --

  --------------------------------------------------------------------------------

  ------------------------------------------------------------------------------------
  **Print Services Role not    Role        Role        Role         Role installed, 
  Role             installed   installed   installed   installed    configured, and 
  Installation**               with issues correctly   and          documented      
                                                       configured   thoroughly      
  ---------------- ----------- ----------- ----------- ------------ --------------- --

  ------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Printer      No          Installer    Installer   Installer   Installer      
  Installer      installer   conversion   converted   converted   converted,     
  Conversion**   found       attempted    but not     and used    used, and      
                             but failed   used                    documented     
                                                                  well           
  -------------- ----------- ------------ ----------- ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Network      Printer    Deployment   Printer      Printer     Printer        
  Printer        not        failed       deployed but deployed    deployed,      
  Deployment**   deployed                not          correctly   tested, and    
                                         functional               documented     
                                                                  well           
  -------------- ---------- ------------ ------------ ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 2: Monitoring Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ------------------------------------------------------------------------------
  **Event   Event     Opened but  Logs reviewed Logs        Logs reviewed     
  Viewer    Viewer    no logs     but           reviewed    with thorough     
  Usage**   not       reviewed    superficial   with some   analysis and      
            opened                              analysis    documentation     
  --------- --------- ----------- ------------- ----------- ----------------- --

  ------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Performance   Performance   Opened but  Metrics     Metrics     Metrics       
  Monitor Usage** Monitor not   no metrics  monitored   monitored   monitored,    
                  opened        monitored   but not     with some   analyzed, and 
                                            analyzed    analysis    documented    
                                                                    thoroughly    
  --------------- ------------- ----------- ----------- ----------- ------------- --

  ----------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Print       Console   Opened but      Active jobs     Active    Active jobs   
  Management    not       functionality   viewed          jobs      viewed and    
  Console       opened    not used        superficially   viewed    documented    
  Usage**                                                 with some thoroughly    
                                                          detail                  
  ------------- --------- --------------- --------------- --------- ------------- --

  ----------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 3: Exploring Third-Party Tools**                                        
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Research   No tools     Research     Research on Research on  Research on    
  on Tools**   researched   incomplete   one tool    two tools    two tools,     
                                         completed   with some    detailed       
                                                     analysis     analysis, and  
                                                                  comparison     
  ------------ ------------ ------------ ----------- ------------ -------------- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------
  **Installation    Tool not    Installation   Tool         Tool         Tool           
  and               installed   failed         installed    installed    installed,     
  Configuration**                              but not      and          configured,    
                                               configured   configured   and documented 
                                                            with issues  thoroughly     
  ----------------- ----------- -------------- ------------ ------------ -------------- --

  ----------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------
  **Reporting   No report   Report   Report      Report      Comprehensive     
  Findings**    generated   lacks    generated   generated   report with       
                            detail   but lacks   with some   thorough analysis 
                                     analysis    analysis    and documentation 
  ------------- ----------- -------- ----------- ----------- ----------------- --

  -------------------------------------------------------------------------------
