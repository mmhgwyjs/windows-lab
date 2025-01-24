# Windows Lab

> Please note that this project is ongoing and is meant solely for learning purposes. Your feedback would be greatly appreciated, as I am using this opportunity to learn.

## Objective

To set up and configure a Windows Server environment to demonstrate essential server administration tasks and services. This project will include configuring Active Directory, DNS, DHCP, and other relevant services, as well as implementing security measures and managing user access.

## Initial Setup

***1. Installing hypervisor.***
   
- You can use either VMware Workstation or VirtualBox, based on your preference. More details [here](https://github.com/mmhgwyjs/homelab?tab=readme-ov-file#hypervisor).

***2. Getting Windows Server ISO.***
   
- [Windows Server 2022 (180-day evaluation)](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022)

- [Windows Server 2019 (180-day evaluation)](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)

  > The evaluation period can be extended, you can check how to do it [here](https://serverdecode.com/extend-evaluation-period-windows-server/). You can extend it 5 times, equivalent to 900 days or approximately 2.5 years.
  
***3. Getting Windows 10 ISO.***
   
- [Windows 10 Enterprise (90-day evaluation)](https://www.microsoft.com/en-us/evalcenter/download-windows-10-enterprise)

  > Evaluation period can be extended, you can check it [here](https://pupuweb.com/solved-fix-reset-extend-windows-trial-expired/). I'm not sure how many times, but there's a limit on extending the evaluation. I've read that you can rearm it three times [here](https://answers.microsoft.com/en-us/windows/forum/all/what-is-the-meaning-of-the-term-rearm-count/203d0add-50dd-45b0-be3b-23f9ac55c560), but I haven't tested it yet.
    
- [Windows 10 Pro (No expiration)](https://www.microsoft.com/en-us/software-download/windows10)

***4. Creating the virtual machines.***

> I use VMware Workstation for this, but the same concept can be applied to VirtualBox.

- Go to `File` then select `New Virtual Machine`.

  ![image](https://github.com/mmhgwyjs/malware-analysis-lab/assets/159692853/22ab3330-bc2d-43ff-9d8f-ff34d7bde957)

- Select `Typical`. Under `Installer disc image file (ISO)`, locate your downloaded Windows OS ISO. Then proceed to `Easy Install`.
  
  ![image](https://github.com/user-attachments/assets/e371e295-3013-4194-ade7-8b104b1040a0)

- We can leave the product key blank and select the Windows version we need. For this guide, we will use `Windows Server 2022 Standard`
  
  ![image](https://github.com/user-attachments/assets/feb9feec-21e5-441b-852d-91a05fad70c1)

- For the disk size and hardware settings, you can adjust them according to your preferences.

  ![image](https://github.com/user-attachments/assets/ec6258b5-18cd-404c-a341-e361f678ba48)

***5. Installing Windows Server/Client OS.***

- If you encountered an error regarding `Microsoft Software License Terms`, we can fix that by removing the `Floppy` drive of the VM.

  ![image](https://github.com/user-attachments/assets/ed699754-763a-4ae5-8983-bb9b86f1f598)

  ![image](https://github.com/user-attachments/assets/9db91aed-bf57-40ad-9c64-35431098c4ab)

  > To modify VM settings, we need to turn off the VM first.

- Now, we can start the actual installation.

  ![image](https://github.com/user-attachments/assets/485cacea-f7db-4328-93f8-75d272bb7554)
  
  ![image](https://github.com/user-attachments/assets/fa5bc503-d78b-4967-a0cb-90e172a3f60f)

- Choose the option with `Desktop Experience` to get the full Windows graphical environment.

  ![image](https://github.com/user-attachments/assets/59c7ed57-c5e4-423f-94d2-ecc1c57a746c)

- It will be pretty straightforward from here, and we'll just need to wait for it to be installed. Select `Custom` for installation type.

  ![image](https://github.com/user-attachments/assets/ddac750d-5bd3-48cb-8f7c-8318f742693d)

***5. Installing VMWare Tools.***

- Select `VM` > `Install VMware Tools`.

  ![image](https://github.com/user-attachments/assets/e117eef8-5b95-4ba8-8368-8e8c4e71f9c7)

- It should appear under `D:` drive.

  ![image](https://github.com/user-attachments/assets/ca879366-0eb3-426c-9190-c1a610fee119)

  ![image](https://github.com/user-attachments/assets/def85db0-74ef-484a-9840-0a4c4a66ee39)

- Select `Typical` setup.

  ![image](https://github.com/user-attachments/assets/9dd0e7a2-bfa9-44fe-8e21-a237476d98c5)

- Restart the machine after.

  ![image](https://github.com/user-attachments/assets/a04bea78-6df4-4adf-8429-7ecc6d6a18d8)

  ![image](https://github.com/user-attachments/assets/79b3811a-fa46-4a52-ad51-c34cd67a2edc)

  > Repeat all the steps above for Windows Client installation.

#### ***Great job! We now have a Windows machine up and running. Let's move on to the practical exercises outlined below.***

## Lab Exercises

| Exercise                   | Description                                                                                     | Link                                                      | Status       |
|----------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------|--------------|
| Setting Up Active Directory | Configure Active Directory on a Windows server, including domain setup, users, and group policies. | [View Exercise](https://github.com/mmhgwyjs/windows-lab/blob/main/Lab%20Exercises/Active%20Directory.md)                                         | Planned  |
| Installing and Configuring IIS Web Server | Set up and configure an IIS Web Server on a Windows machine, including website hosting and management. | [View Exercise](https://github.com/mmhgwyjs/windows-lab/blob/main/Lab%20Exercises/IIS%20Web%20Server.md)                                         | Planned  |
