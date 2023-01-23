---
title:  "Step by step guide – How to install Kali Linux on VMware"
author: Rupesh Bhandari
date:   2021-01-15 16:15:00 +0545
categories: [Linux, Kali, Vmware, TUTORIAL] 
tags: [Kali Linux, VMWARE] 
---

<!-- Bla bla <sup id="a1">[1](#f1)</sup> -->

In this post, I will show you how to install the latest version of Kali Linux (2021.1)[^1] on VMware Workstation 16 Pro [^2]. This will allow you to have a Kali virtual machine as a guest operating system on your host machine. This way of using Kali is very effective and used by a lot of people.

Kali was built and is maintained by (<a href="https://www.offensive-security.com/" target="_blank">Offensive Security</a>), it has hundreds of tools available for security auditing, penetration testing and ethical hacking. Below are the steps for installing Kali Linux: –

1. Download the iso file for Kali Linux

    Go to the <a href="https://www.kali.org/downloads/" target="_blank">Official Kali Linux website</a> and browse to the downloads section. From the download page, download the 64-bit or 32-bit installer based upon your system configuration.

    ![Step 1](/assets/img/kalionvm/1.jpg)

2. Open VMware Workstation and click on “Create a New Virtual Machine”

    In VMware, click on File -> New Virtual Machine or click on Create a New Virtual Machine from Home. This will open the “New Virtual Machine Wizard”.

    ![Step 2](/assets/img/kalionvm/2.png)

3. “New Virtual Machine Wizard” dialogue box opens

    The configuration wizard will have two options. “Typical” is for creating a virtual machine with default settings. “Custom” is for advanced options like <a href="https://en.wikipedia.org/wiki/SCSI" target="_blank">SCSI Controller</a> type, virtual disk type, etc. We will choose the default i.e. “Typical” configuration.

    ![Step 3](/assets/img/kalionvm/3.jpg)

4. Select the installation source

    Browse to the downloaded iso file on your system and click Next. VMware usually detects the operating system in the disc image (iso file), but not with Kali Linux. So, ignore the warning and proceed further.

    ![Step 4](/assets/img/kalionvm/4.jpg)

5. Select the guest operating system

    Select Linux as the guest operating system. Choose <a href="https://www.debian.org/" target="_blank">Debian</a> 9.x 64-bit or 32-bit based on your system configuration and click Next.

    ![Step 5](/assets/img/kalionvm/5.jpg)

6. Virtual machine name and location

    Enter a name for your virtual machine. You can choose the default location which will be Documents\Virtual Machines or you can choose any other location.

    ![Step 6](/assets/img/kalionvm/6.jpg)

7. Specify Disk Capacity

    The maximum disk size is the maximum space that your virtual machine can utilize after it is created. You can choose the recommended size of 20 GB if your requirements are not much. Otherwise, you can increase the size if you plan on installing heavy software on your virtual machine. This has to be done based upon your system’s configuration.

    You can store the virtual disk as a single file on your computer or split it into multiple files. The flexibility to move your virtual machine from one computer to another will be better with the second option. The performance will be reduced though will larger disk files.

    ![Step 7](/assets/img/kalionvm/7.jpg)

8. Ready to Create Virtual Machine

    The dialogue box will show the virtual machine settings that you chose in the previous steps. You can proceed with these settings and click Finish, or you can choose to Customize Hardware.

    ![Step 8.1](/assets/img/kalionvm/8.1.jpg)

    You can increase the RAM allocated to the virtual machine using the slider. Choose a higher value only if your host machine has enough RAM. You can also increase the number of processors and the number of cores per processor. Again, this depends on whether your host machine has enough processing power.

    After you are done, click on Close and then click on Finish.

    ![Step 8.2](/assets/img/kalionvm/8.2.jpg)

9. Power on the virtual machine

    Click on “Power on this virtual machine” to start the newly created virtual machine.

    ![Step 9](/assets/img/kalionvm/9.jpg)

10. Kali Linux installer menu

    After you start the virtual machine, the Kali Linux installer menu will appear. Select “Graphical install” from the given options and continue.

    ![Step 10](/assets/img/kalionvm/10.jpg)

11. Select a language

    The default language is English, select any other language if you want to, for the installation process and the operating system.

    ![Step 11](/assets/img/kalionvm/11.jpg)

12. Select your location

    Select the location which will be used to set the time zone of your operating system and other location-based settings.

    ![Step 12](/assets/img/kalionvm/12.jpg)

13. Configure the keyboard

    Select the keyboard for your Kali Linux. By default, this is set to American English. 

    After you click Continue, installer components will be loaded from installation media.

    ![Step 13](/assets/img/kalionvm/13.jpg)

14. Configure the network

    Enter a hostname for your Kali Linux. Since this is a home network, you can type anything.

    ![Step 14.1](/assets/img/kalionvm/14.1.jpg)

    Next, the installer will ask you for a domain name. You can enter anything or simply leave this empty and continue.

    ![Step 14.2](/assets/img/kalionvm/14.2.jpg)

15. Set up users and passwords

    Enter the name for your user account and click Continue.

    ![Step 15.1](/assets/img/kalionvm/15.1.jpg)

    In the next step, enter a username for the new account.

    ![Step 15.2](/assets/img/kalionvm/15.2.jpg)

    Create and enter a password for your new account. Then click on Continue.

    ![Step 15.3](/assets/img/kalionvm/15.3.jpg)

16. Partition disks

    Select the default option “Guided – use entire disk” and click Continue.

    ![Step 16.1](/assets/img/kalionvm/16.1.jpg)

    In the next step, select the timezone for your region.

    ![Step 16.2](/assets/img/kalionvm/16.2.jpg)

    Select the partitioning scheme, choose “All files in one partition” which is recommended for new users.

    ![Step 16.4](/assets/img/kalionvm/16.4.jpg)

    The next window will show you the details of your configured partitions. Select “Finish partitioning and write changes to disk” and click Continue.

    ![Step 16.5](/assets/img/kalionvm/16.5.jpg)

    To write changes to the disk click on “Yes” and then click Continue.

    ![Step 16.6](/assets/img/kalionvm/16.6.jpg)

17. Installation of the base system

    The installation will begin in this step. Wait for it to complete and then proceed further.

    ![Step 17](/assets/img/kalionvm/17.jpg)

18. Configure the package manager

    The dialogue box will now ask for HTTP proxy information. You can leave this blank and click Continue.

    ![Step 18.1](/assets/img/kalionvm/18.1.jpg)

    The installation process will continue after that proceed further.

    ![Step 18.2](/assets/img/kalionvm/18.2.jpg)

19. Select and install software

    In this step, choose the software to install apart from the core of the system. Select a desktop environment and other tools to install.

    ![Step 19.1](/assets/img/kalionvm/19.1.jpg)

    The selected software will be installed now. This step can take hours to complete depending on the software you have selected. If you only choose the defaults, the installation will be finished in much less time.

    ![Step 19.2](/assets/img/kalionvm/19.2.jpg)

20. Install the GRUB boot loader

    Click “Yes” to install the GRUB boot loader and then click Continue.

    ![Step 20.1](/assets/img/kalionvm/20.1.jpg)

    Select the device shown for boot loader installation and click Continue.

    ![Step 20.2](/assets/img/kalionvm/20.2.jpg)

    The GRUB boot loader will be installed now.

    ![Step 20.3](/assets/img/kalionvm/20.3.jpg)

21. Finish the installation

    The complete installation will be done.

    ![Step 21.1](/assets/img/kalionvm/21.1.jpg)

    The installation is complete now. Click on Continue after which your virtual machine will reboot. After the reboot, you will be able to use your newly installed Kali Linux.

    ![Step 21.2](/assets/img/kalionvm/21.2.jpg)

22. Kali ready to use

    Enter the username and password that you created during the installation to log in.

    ![Step 22.1](/assets/img/kalionvm/22.1.jpg)

    Now you are logged in into your Kali desktop which is ready to use.

    ![Step 22.2](/assets/img/kalionvm/22.2.jpg)

I hope this tutorial was helpful. Stay tuned for more updates! 🙂

References:

[^1]: Kali Linux 2021, <a href="https://www.kali.org/blog/kali-linux-2021-1-release/" target="_blank">https://www.kali.org/blog/kali-linux-2021-1-release/</a>
[^2]: VMware Workstation, <a href="https://en.wikipedia.org/wiki/VMware_Workstation" target="_blank">https://en.wikipedia.org/wiki/VMware_Workstation</a>
