![image](https://github.com/user-attachments/assets/0d0fd663-f40c-4e31-bfc4-1142236c7111)


# SYSADM1 -- Setting Up Webserver

# Requirement: 

-   A virtual machine running Linux and Windows OS

    Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

    ![](./image2.png){width="5.688906386701662in"
    height="3.8566951006124235in"}

2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

        ![](./image3.png){width="5.594530839895013in"
        height="3.0941819772528434in"}![](./image4.png){width="5.6674573490813644in"
        height="3.3858891076115487in"}

3.  Configure the Website:

    -   Right-click on your website and select Edit.

    -   Set the Default Document to the name of your main HTML file
        \>default.html

        ![](./image5.png){width="3.333798118985127in"
        height="2.698292869641295in"}

    -   Configure other settings as needed (e.g., SSL certificates,
        authentication)

4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

        ![](./image6.png){width="3.652083333333333in"
        height="1.52377624671916in"}

    -   Save it as default.html or your preferred name.

5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

![](./image7.png){width="7.027083333333334in" height="6.0625in"}

![](./image8.png){width="7.027083333333334in"
height="7.2340277777777775in"}

Grading Rubric

  ------------------------------------------------------------------------------
  **Criteria**      **Points**   **Description**
  ----------------- ------------ -----------------------------------------------
  Web Server        15           Correctly installs IIS or another web server on
  Installation                   the virtual machine.

  Website           15           Successfully configures the website with the
  Configuration                  correct physical path, IP address, port, and
                                 default document.

  Successful Access 15           Successfully accesses the web page from the
                                 client computer using the correct URL.

  Troubleshooting   15           Demonstrates ability to troubleshoot common
                                 issues, such as network connectivity problems
                                 or configuration errors.

  Documentation     10           Provides clear and concise documentation of the
                                 installation, configuration, and testing
                                 process.

  Total             /70          
  ------------------------------------------------------------------------------
