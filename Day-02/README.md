Day 02 - Installing Kali Linux on Oracle VirtualBox
Date-18-07-2025

Today’s session focused on setting up Kali Linux in a virtual environment using Oracle VirtualBox. Below is a step-by-step guide on how to install and configure everything correctly.

Pre-requisites:
To install Kali Linux on a Windows host machine, you’ll need three essential tools:

Kali Linux VirtualBox Image
Download the latest VirtualBox image from the official Kali website:
Download Kali Linux VirtualBox Image

Oracle VirtualBox
Download and install Oracle VirtualBox, a free and open-source virtualization software:
Download Oracle VirtualBox

7Zip
A tool for extracting compressed files. Download it from:
Download 7Zip

Note: Ensure you have at least 10–15 GB of free storage space on your system for the installation.

Step-by-Step Installation:
Step 1: Install Oracle VirtualBox
Run the downloaded VirtualBox installer file.

When prompted, click "Yes" to grant administrator privileges.

In the installation dialog box, click Next.

On the Custom Setup page, leave the default settings and click Next.

The Network Interface Warning will appear. Click Yes to proceed.

The Missing Dependencies dialog may pop up. Click Yes to install any required dependencies.

When you reach the "Ready to Install" page, click Install.

Once installation is complete, click Finish to close the setup and launch Oracle VirtualBox.

Troubleshooting Common Issues:
Missing Microsoft Visual C++ Redistributable (x64) 2015-2022
If you encounter an error about missing dependencies, download and install the required Visual C++ package from:
Download Microsoft Visual C++ Redistributable
After installation, relaunch the Oracle VirtualBox installer.

AMD-V Disabled in BIOS
If you encounter a virtualization error (AMD-V or VT-x is disabled), follow these steps:

Reboot your system and enter BIOS settings (check your device’s model for the correct BIOS entry key, such as F2, F12, DEL, etc.).

In BIOS, locate Virtualization or SVM Mode (in Advanced Settings) and enable it.

Save changes and reboot.

Step 2: Install 7Zip
Right-click the downloaded 7Zip installer and select "Run as Administrator".

In the installation dialog, click Install.

Once done, click Close.

Step 3: Extract the Kali Linux Image
Navigate to the folder where you’ve downloaded the Kali Linux VirtualBox image (.7z file).

Right-click the ZIP file and select “Show more options” > 7Zip > Extract Here.

Wait for the extraction to complete.

Step 4: Load the Kali Linux VirtualBox Image
(Optional but Recommended): For better performance and organization, create a separate partition on your disk (10–15 GB is sufficient). Here’s a guide on creating a partition.

Copy the extracted Kali Linux VirtualBox image files into the new partition.

In the folder, you’ll see two types of files:

VirtualBox Machine Definition (a .vbox file)

Virtual Disk Image (a .vdi file)

Double-click on the VirtualBox Machine Definition (.vbox) file. This will open Oracle VirtualBox.

In VirtualBox, click Start to boot the virtual machine. The first boot may take some time.

Once Kali Linux boots up successfully, you can log in with the username kali and the password kali.

Summary:
By the end of the session, we successfully installed Oracle VirtualBox, extracted the Kali Linux image, and launched Kali Linux in a virtual machine. This setup provides a safe, isolated environment for practicing penetration testing and ethical hacking without affecting the host machine.
