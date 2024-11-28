+----------------------------------+---------------------------+------+
| ![](vertopal_                    |                           |      |
| d71cd5380e29450596510a51c27cdd6c |                           |      |
| /media/image1.png){width="2.4in" |                           |      |
| height="0.5881944444444445in"}   |                           |      |
|                                  |                           |      |
| SCHOOL OF INFORMATION AND        |                           |      |
| TECHNOLOGY                       |                           |      |
+----------------------------------+---------------------------+------+
| NAME: Aaron Joshua G. Sese       | DATE PERFORMED: August    |      |
|                                  | 28, 2024                  |      |
+----------------------------------+---------------------------+------+
| Section: IDC2                    | DATE SUBMITTED: August    |      |
|                                  | 28, 2024                  |      |
+----------------------------------+---------------------------+------+

# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

+------+------------------+-------------------------------------------+
| **   | **Name of        | **Screenshot**                            |
| Stat | Service**        |                                           |
| us** |                  |                                           |
+======+==================+===========================================+
| S    | Dev              | ![](verto                                 |
| tart | icePicker_7c03da | pal_d71cd5380e29450596510a51c27cdd6c/medi |
|      |                  | a/image2.png){width="3.920138888888889in" |
|      |                  | height="1.8618055555555555in"}            |
|      |                  |                                           |
|      |                  | ![](vertop                                |
|      |                  | al_d71cd5380e29450596510a51c27cdd6c/media |
|      |                  | /image3.png){width="4.2912423447069115in" |
|      |                  | height="0.2621347331583552in"}            |
+------+------------------+-------------------------------------------+
| Stop | Dev              | ![](vertop                                |
|      | icePicker_7c03da | al_d71cd5380e29450596510a51c27cdd6c/media |
|      |                  | /image4.png){width="3.8859590988626422in" |
|      |                  | height="1.7814982502187227in"}            |
+------+------------------+-------------------------------------------+
| Res  | Dev              | ![](verto                                 |
| tart | icePicker_7c03da | pal_d71cd5380e29450596510a51c27cdd6c/medi |
|      |                  | a/image5.png){width="3.920138888888889in" |
|      |                  | height="1.7944444444444445in"}            |
+------+------------------+-------------------------------------------+
| P    | MySQL83          | ![](vertop                                |
| ause |                  | al_d71cd5380e29450596510a51c27cdd6c/media |
|      |                  | /image6.png){width="3.9987478127734035in" |
|      |                  | height="1.8229593175853018in"}            |
+------+------------------+-------------------------------------------+

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image7.png){width="2.8227340332458444in"
> height="3.254856736657918in"}
> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image8.png){width="2.8125360892388453in"
> height="3.2203543307086613in"}
>
> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image9.png){width="3.024037620297463in"
> height="3.5242563429571305in"}
> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image10.png){width="3.0335214348206474in"
> height="3.5252384076990375in"}
>
> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image11.png){width="3.0446412948381454in"
> height="3.535463692038495in"}

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image12.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

7.  Save the batch file in Z:\\lastname_timer.bat

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **Replace path_to_your_batch_file.bat with the actual path to your
> batch file.**

9.  Verify that BatchTimerService has been added to the services.

> **SS:**
> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image13.png){width="5.177806211723534in"
> height="0.29170713035870516in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:**
> ![](vertopal_d71cd5380e29450596510a51c27cdd6c/media/image14.png){width="5.604948600174978in"
> height="2.354494750656168in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **/50**                                            
  ---------------------------------------------------------------------------------------
