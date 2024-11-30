+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| a5b0eee26cc943128bcf2466a2689382 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Aaron Joshua G. Sese       | DATE PERFORMED:        | /50      |
|                                  | 11/14/2024             |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 11/14/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

**Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos
manages secure logins through ticket-based access.

**Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

**Step 1: Initial Setup and Package Installation**

1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

*bash*

*sudo apt update && sudo apt upgrade --y*

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image2.png){width="7.027083333333334in"
height="0.4486111111111111in"}

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image3.png){width="5.86540135608049in"
height="0.35421587926509185in"}

2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

*bash*

*sudo apt install krb5-kdc krb5-admin-server --y*

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image4.png){width="7.027083333333334in"
height="0.3902777777777778in"}

3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

*bash*

*sudo apt install krb5-user --y*

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image5.png){width="4.969443350831146in"
height="0.2604527559055118in"}m

-   During installation, when prompted, enter the Kerberos realm you
    plan to set up, e.g., MYLAB.LOCAL.

**Step 2: Configure the Kerberos Server (VM1)**

1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

*bash*

*sudo nano /etc/krb5.conf*

-   Set the realm as MYLAB.LOCAL. You should also specify the KDC and
    admin server as VM1's hostname or IP address:

ini

\[libdefaults\]

default_realm = MYLAB.LOCAL

\[realms\]

MYLAB.LOCAL = {

kdc = \<VM1_IP_or_hostname\>

admin_server = \<VM1_IP_or_hostname\>

}

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image6.png){width="4.594390857392826in"
height="4.646481846019247in"}

-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

*bash*

*sudo krb5_newrealm*

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image7.png){width="7.027083333333334in"
height="0.4548611111111111in"}

-   You will be prompted to set a password for the Kerberos database.

3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:

*bash*

*sudo systemctl start krb5-kdc*

*sudo systemctl start krb5-admin-server*

*sudo systemctl enable krb5-kdc*

*sudo systemctl enable krb5-admin-server*

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image8.png){width="7.027083333333334in"
height="1.961111111111111in"}

**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

*bash*

*sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser.

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image9.png){width="7.027083333333334in"
height="1.2791666666666666in"}

2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

*bash*

*sudo kadmin.local -q \"listprincs\"*

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image10.png){width="6.855123578302712in"
height="1.5939720034995626in"}

**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

*bash*

*sudo nano /etc/krb5.conf*

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set on VM1.

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image11.png){width="7.027083333333334in"
height="4.667361111111111in"}

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit testuser@MYLAB.LOCAL*

-   Enter the password you set for testuser.

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image12.png){width="4.479792213473316in"
height="0.46881561679790024in"}

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*klist*

![](vertopal_a5b0eee26cc943128bcf2466a2689382/media/image13.png){width="7.027083333333334in"
height="1.2694444444444444in"}

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.
