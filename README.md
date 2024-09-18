# Linux-Ass1
First Assignment ACIT 2420

# ACIT 2420 ASSIGNMENT I  
# Chelsie Salome Lele Wambo  
# A01372274  

# CREATING A REMOTE SERVER WITH DigitalOcean  

Follow this tutorial if you are a CIT Term II student getting started with **DigitalOcean** to :  
- Create SSH keys on your local machine.
- Add a custom Arch Linux image using the web console
- Create a Droplet running Arch Linux using the DigitalOcean web console.
- Use a cloud-init configuration file to automate initial setup tasks (e.g., user creation).
- Connect to your server using your SSH keys.  

# Introduction  
## What SSH Keys?  
1. What is SSH (Secure Shell) and why is it commonly used for communication between machines?  
2. What are the benefits of SSH Keys  
3. Why is SSH key-based authentication preferred to password-based authentication  

# Prerequisites  
What you will need:  
* A Linux, macOS, or Windows machine (with Git Bash or PowerShell installed for Windows users).  
* Basic familiarity with the command line. Here are some basic command lines for different OS:
    * [Windows Command Lines](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands#c)  
    * [Mac Command Lines](https://developer.apple.com/library/archive/documentation/OpenSource/Conceptual/ShellScripting/CommandLInePrimer/CommandLine.html)  
    * [Linux Command Lines](https://ubuntu.com/tutorials/command-line-for-beginners#2-a-brief-history-lesson)  

# Step 1: Understanding SSH Key Pairs  
## Private Key  
## Public Key  
## Private Key vs Public Key  

# Step 2: Installing OpenSSH  
OpenSSH is ...
* Check if SSH is installed  
If you have the following versions of OS or newer, then your machine most-likely already have OpenSSH installed:  
    - Windows 10 or Windows 11  
    - macOS 10.13  
    - Most Linux Distros  

# Step 3: Generating an SSH Key Pair  
* ## Windows Users  
> **Note:** The commands below must be typed in the **Windows Terminal**, NOT in the **Windows Powershell**
1. Create an .ssh directory (if not yet created) using the command:
> `mkdir .ssh`  
2. Create the ssh key pair using the command:
`ssh-keygen -t ed25519 -f C:\Users\your-user-name\.ssh\key-name key -C "youremail@email.com"`  
### Explanation of the command:  



 