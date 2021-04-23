---
title: "Get started with WSL"
date: 2021-04-22T21:54:48+05:30
draft: false
author: Sk Saddam Hossain
description: Windows Subsystem for Linux
---

# Windows subsystem for Linux

WSL is an optional feature of Windows 10 which allows the user to run Linux distributions natively on Windows10 without the use of a Virtual Machine. This tool is primarily used by developers and those who work on or with open source projects. You can access the windows file manager through the bash shell in Linux, and run shell scripts and GNU/Linux command-line applications including: 

- Tools – vim, emacs
- Languages – Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc. 
- Services – sshd, MySQL, Apache, lighttpd 
Moreover, it gives access to run command-line software such as grep, sed or ELF 64 binaries. You can also access your local machine’s file system from within the Linux bash shell, you can find the drives mounted in /mnt folder. 

For instance, to access the c: drive: 

```html
  cd /mnt/c:
```

**Why not use a Virtual Machine?** 

- Compared to a VM, it is far less resource-intensive. 

- You can interact with your windows host from your Bash prompt, and also run Linux commands from cmd and PowerShell.

REQUIREMENTS:
In general, WSL requires a 64-bit version of Windows 10 starting from Build 1607 (August 2, 2016 release) or later installed. Further requirements depend on the Linux distribution that you want to use. 
Note: WSL apps only work when installed on the system drive. Launching WSL installed on a different drive will yield an error message.

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