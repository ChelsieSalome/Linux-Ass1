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
## What are SSH Keys?  
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
    * Windows 10 or Windows 11  
    * macOS 10.13  
    * Most Linux Distros  

# Step 3: Generating an SSH Key Pair  
* ## Windows Users  
> **Note:** The commands below must be typed in the **Windows Terminal**, NOT in the **Windows Powershell**
1. Create an .ssh directory (if not yet created) using the command:
> `mkdir .ssh`  
2. Create the ssh key pair using the command:
>`ssh-keygen -t ed25519 -f C:\Users\your-user-name\.ssh\key-name -C "youremail@email.com"`  

**Explanation of the command:**  
* `ssh-keygen`: Command-line utility used to generate, manage and convert SSH keys.  
* `-t`: specifies the **type of key** to generate.  
* `ed25519`: is a type of public-key algorithm. Other options of public key types include: rsa, dsa & ecdsa. Ed25519 is preferred for new keys due to its superior performance, smaller key sizes, better security, and resistance to certain attacks. (VulnerX, 2024) You can refer to [RSA vs ECDSA vs Ed25519](https://vulnerx.com/ssh-key-algorithms/) for further reading about each public key advantages.  
* `f`: option specifies the file name and path where the key pair (both the private and public key) will be saved.  
* `C:\Users\your-user-name\.ssh\key-name`: is the full path on a Windows system where the key files will be stored, please replace `your-user-name` with the actual **user name** as displayed on the terminal, and `key-name` with the **key name** that you would have chosen for your key:
        * The private key will be saved as `key-name`.  
        * The public key will be saved as `key-name.pub`.  
* `C`: option adds a comment to the key.  
    * `"youremail@email.com"`: is the comment added to the key. This comment is embedded in the public key file and is visible when the key is used. It's helpful for recognizing which key belongs to whom, especially when managing multiple keys on servers or services like GitHub.  
    * **Example**: Let's say your username is Chelsie, your email address is "chelsie@gmail.com"  and you choose to name your key "git-key", then the command to create your SSH key pair might look like this:
    > `ssh-keygen -t ed25519 -f C:\Users\tom\.ssh\git-key -C "chelsie@gmail.com"`  

## macOS & Linux Users  
You don't have to manually create an .ssh directory as running the `ssh-keygen` command will automatically do that.  
* Open your terminal and type:  
> `ssh-keygen -t ed25519 -f ~/.ssh/key-name -C "youremail@email.com"`  
**Explanation of the Command:** 
* The command is similar to the Windows-command, the only difference is the path.  
* `-f ~/.ssh/key-name`: This tells ssh-keygen where to save the generated private key. It will create the .ssh directory if it does not already exist and place key-name and key-name.pub (the private and public keys, respectively) inside it. (macOS & Linux use the tilde ~ to represent the user's home directory).  


# Step 4: Choosing a Passphrase  
You can protect the private using a **passphrase**. A **passphrase** is ............  
Because we are just using this for a small project, and to simplify your life ie to not have to remember about passphrases, I just to not set a passphrase and just hit **ENTER** twice.............  

# Step 5: Verifying your SSH Keys  
1. type `cd .ssh` > `ls` to view the files in the .ssh directory.  
> The keys are successfully created if you see the following files in the .ssh directory:  
* **key-name** *(private key)*  
* **key-name.pub** *(public key)*  






 