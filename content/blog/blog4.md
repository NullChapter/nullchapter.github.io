---
title: "Cyber Attack"
date: 2021-10-08T02:55:48+05:30
draft: false
author: Sk Saddam Hossain
description: Windows Subsystem for Linux
---

If you are a cybersecurity expert living in today’s shark-infested cyber-world, your mission is to stay ahead of the bad guys and keep your activity safe. This starts by understanding your vulnerabilities, knowing the many ways by which your resistance can be breached, and then putting together in position the protections needed to maintain a secure, tough cybersecurity posture. It’s a big job and is significantly important to the security of your enterprise. Cybercrimes have increased every year as people try to profit from vulnerable business system. Often, attackers are look for liberate 53 percent of cyber-attack resulted in damage. Cyberthreats can also be launched with ulterior motives. Some attackers look to demolish systems and data as a form of “Hacktivism.”
Here are three key term that lie at the heart of all enterprise cyber-defenses:

- Attack surface
- Cyber Attack vector
- Security breach


**Attack Surface** 

The sum-total of point on a network where attack can occurs where and not permitted user (the “attacker”) can try to manipulate or take out data using a many of breach methods (the “cyber attack vectors”). If you consider a graph where  as the x-axis lists all of the devices and apps on your network (infrastructure, apps, endpoints, IoT, etc.) and the y-axis are the different breach methods such  weak and default passwords, reused passwords, phishing, social engineering, unpatched software, mis configurations etc. – the plot is your [**attack surface**](https://www.balbix.com/insights/attack-vector-vs-attack-surface/)

**Steps to Install Windows Subsystem for Linux (WSL)**

Before installing any Linux distribution for WSL, you must ensure that the “Windows Subsystem for Linux” optional feature is enabled in your system.
If not you can enable it in two ways. 

**Graphically**

- Open “Settings”. 
- Go to “Apps -> Apps & Features”.
- Scroll down to the “Programs and Features” link: 
- Click the link. The Programs and Features dialogue will be opened.
- On the left, click the link Turn Windows features on or off.
    ![> null_](/blog/blog2/1.png)

- 'Windows Features' window will appear on the screen. Scroll down to the option named “Windows Subsystem” for Linux and enable it.
    ![> null_](/blog/blog2/2.png)
- Click OK to apply the changes you made.
- Reboot the operating system when prompted. 

**Using Powershell:**
- Open PowerShell as Administrator and run the below command: 
```html
  Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```
- Restart your computer when prompted. 

Finally, you are ready to install the Linux distribution of your choice. To download and install the preferred distro:
- Make sure that your system has Windows 10 build 16215 or later. Go to Settings>System>About and look for the **OS Build** and **System Type** fields. 
    ![> null_](/blog/blog2/3.png)

- Open Microsoft Store and choose your Linux distro you want to use. The following link will take to the Microsoft Store for each specific distribution: 
    - [**Ubuntu 16.04 LTS**](https://www.microsoft.com/en-in/p/ubuntu-1604-lts/9pjn388hp8c9?rtc=1&activetab=pivot:overviewtab) 
    - [**Ubuntu 18.04 LTS**](https://www.microsoft.com/en-in/p/ubuntu-1804-lts/9n9tngvndl3q?rtc=1&activetab=pivot:overviewtab)
    - [**OpenSUSE Leap 15**](https://www.microsoft.com/en-in/p/opensuse-leap-15/9n1tb6fpvj8c?rtc=1&activetab=pivot:overviewtab)
    - [**OpenSUSE Leap 42**](https://www.microsoft.com/en-in/p/opensuse-leap-42/9njvjts82tjx?rtc=1&activetab=pivot:overviewtab)
    - [**SUSE Linux Enterprise Server 12**](https://www.microsoft.com/en-in/p/suse-linux-enterprise-server-12/9p32mwbh6cns?rtc=1&activetab=pivot:overviewtab)
    - [**SUSE Linux Enterprise Server 15**](https://www.microsoft.com/en-in/p/suse-linux-enterprise-server-15/9pmw35d7fnlx?rtc=1&activetab=pivot:overviewtab)
    - [**Kali Linux**](https://www.microsoft.com/en-in/p/kali-linux/9pkr34tncv07?rtc=1&activetab=pivot:overviewtab)
    - [**Debian GNU/Linux**](https://www.microsoft.com/en-in/p/debian/9msvkqc78pk6?rtc=1&activetab=pivot:overviewtab)
    - [**Fedora Remix for WSL**](https://www.microsoft.com/en-in/p/fedora-remix-for-wsl/9n6gdm4k2hnc?rtc=1&activetab=pivot:overviewtab )
    - [**Pengwin**](https://www.microsoft.com/en-in/p/pengwin/9nv1gv1pxz6p?rtc=1&activetab=pivot:overviewtab)
    - [**Pengwin Enterprise**](https://www.microsoft.com/en-in/p/pengwin-enterprise/9n8lp0x93vcp?rtc=1&activetab=pivot:overviewtab)
    - [**Alpine WSL**](https://www.microsoft.com/en-in/p/alpine-wsl/9p804crf0395?rtc=1&activetab=pivot:overviewtab)
    
    *You may have to pay for some of the listed distros.*

- From the distro’s page you opened in the Microsoft Store, select “Get”. 
    ![> null_](/blog/blog2/4.png)
After installation is complete, click Launch.

**A few common ERRORS**

✗ **Error: 0x8007019e WslRegisterDistribution failed**
- This error pops up if you have not enabled the “Windows Subsystem for Linux” optional feature. To fix it follow the procedure provided at the start of the document. 

✗ **Error: 0x80070003 during Installation**
- The Windows Subsystem for Linux only runs in system drive (i.e. usually your c: drive). Hence, make sure that the distros you have installed are stored in your system drive. 
- Open Settings->Storage->More Storage Settings: Change where new content is saved
    ![> null_](/blog/blog2/5.png)

✗ **Error: 0x80040306 during Installation**
This pops up because WSL does not support legacy consoles. To turn off the legacy console:
- Open “Command Prompt” 
- Right-click on the title bar > Properties > Uncheck “Use legacy console”. III. Click OK 
✗ Error: 0x80040154 after Windows Update 
During windows update the windows feature of “WSL” may get disabled to default. To fix it follow the steps explained in the first error.

Once the installation is complete, you will be asked to create a user account. The username and password can be different from your Windows system.
    ![> null_](/blog/blog2/6.png)

Update your Linux distro: 
```html
Sudo apt update
Sudo apt upgrade
```
 
Now, you are all set.

With Love,

Sk Saddam Hossain

- **https://sksaddam.com**
- [**LinkedIn**](https://www.linkedin.com/in/sksaddam/)
- [**GitHub**](https://github.com/SaddySk/)