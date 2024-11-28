+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| d6961b36a9d7409890a6400c7eb07f2a |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: Aaron Joshua G. Sese       | DATE PERFORMED:        |          |
|                                  | September 12, 2024     |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | September 12, 2024     |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image2.png){width="4.135416666666667in"
height="1.8020833333333333in"}

Complete this lab as follows:

1.  Use the service --status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  alsa-utils.service                     bluetooth.service

  anacron.service                        console-setup.sh.service

  apparmor.service                       grub-common.service

  apport.service                         keyboard-setup.sh.service

  cron.service                           plymouth.service
  -----------------------------------------------------------------------

SS:

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image3.png){width="5.834146981627296in"
height="1.8335892388451445in"}

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image4.png){width="2.0315332458442694in"
height="0.3021259842519685in"}

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image5.png){width="2.7608016185476814in"
height="0.2396172353455818in"}

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image6.png){width="1.5939720034995626in"
height="0.2500349956255468in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image7.png){width="4.359946412948381in"
height="1.1875in"}

3.  Check the status of the Bluetooth service. What is its status?

SS:
![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image8.png){width="7.027083333333334in"
height="3.0541666666666667in"}

**There was an error in starting the bluetooth. It said that the
bluetooth file is not in the directory /sys/class/bluetooth**

4.  Check the status of the cups services. Since when was it running?

SS:
![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image9.png){width="7.027083333333334in"
height="3.2444444444444445in"}

**It started running at September 12, 9:07 am.**

5.  Stop cups services.

6.  Verify if the service was stopped.

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image10.png){width="1.2293383639545057in"
height="0.28128937007874016in"}

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image11.png){width="7.027083333333334in"
height="0.5722222222222222in"}

7.  Restart the cups services

8.  Verify if the service was restarted.

![](vertopal_d6961b36a9d7409890a6400c7eb07f2a/media/image12.png){width="7.027083333333334in"
height="0.44583333333333336in"}

**The service was restarted as the time for it to start was changed.**
