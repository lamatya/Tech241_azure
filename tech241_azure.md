Azure Week
Day1

What is cloud?

The cloud is a service and resources that are available on demand.

Types of Clouds

- Private cloud -dedicated to privated company or hosted by the third party company. they own the data centre where they rent those servers its there own private cloud. It can also be used when there is no internet access example cruise

- Public Cloud - we shre the cloud with rest of the public

- Hybrid Cloud- It is a mix of on premises and cloud together. 

- MUlti-coud - using two different cloud providers. 

Shared responsibility (Concepts)

On premises
IAAS (infrastructure as a service)
PAAS (platform as a service) –  SQL service data base
SAAS – you only need to manage data; As you don’t need to worry managing other shared responsibilities as it is managed by the cloud


What are some advantages/disadvantages of using the cloud?

Advantages; 
- guranteed uptime services esp AZURE.
- total cost of ownership. 
- Scalability
- Secure

Disadvantages:

- Requires internet
- Data loss
- Can have security concerns

What are disadvantages of using hybrid cloud or multi-cloud?
Difficulty of Implementation.
Security Concerns.
Visibility.
Compatibility.
Expense.
Cost savings.
Control.
Scalability and Deployment.



On-prem vs cloud: What usually cheaper for a organisation? Explain

Cloud is cheaper on a longer run as they can buy severs in a bulk. And also depends upon the services required. 


Which cloud provider is the best? Why?
Amazon Web's cloud-computing services can be considered the best cloud platform. Amazon Web has different types of cloud computing, which can be suitable for any business. Considering their quality of service and virtual machines, Amazon Web can serve your needs if you are looking for cloud providers



AZURE

What is AZURE?

Tenant Root Group.

Management groups- where you can insure complience, set policies, permissions. A way of enforcing complience. You can also have management groups under management groups ( there can be 6 levels)

Subscription- this is a way to separate billing. There is a limit/quota in subscritpion. Each subscription(student subscription, pay as you go subscritpion)

Resource groups- It is like a containers. We cannot have resource groups under resources. You can have resource group under managements. AWS doesnt require resource group. AZURE must have resourcegroup in order to create resources. 

Resources- it goes inside of the resource groups. 


CapEx and OpEx

CapEx- Capital Expenditure- you have to pay for it now. Big expense- mostly with on prem but still have to maintain and pay for other services
OpEx- spread out the cost/ monthly payment may help in budgeting/planning. 

Tags--->> it is a big thing in azure. if you tag your resources in azure as it helps to group things in the billing. 


ARM - is like API. ARM is like a azure use manager. they always have new updates and to keep with the updates you need CLI and powershell.  

ARM- PORTAL-CLI-POWERSHELL-TF ( they all have to go through ARM (Azure Resource Manager)).

# Creating the VM

- Create .ssh Key on GIT Bash

- Make the Resource group named- tech241

- Make a key pair name: tech241-larisha-az-key

- upload ssh Key


## On Microsoft Azure,

-Sign in

-Search for Virtual Machine, Select Virtual Machine

-Once you select VM select create Azure Virtual MAchine

-Name the resource Group as tech241

-Name the VM as tech241-larisha-mann-app

-Select the region as UK South

-Select Security as Standard

-Use Uburto pro 18.04 LTS

-Select size as standard B1s 

-Use username as adminuser

-For ssh public key source: use existing key stored in azure

-select tech241-larisha-az-key as stored keys


## for the inbound port rules- you have to select ssh and http (both)


## on tags, name as owner and value as larisha and select review and create.



### Git bash to create ssh key and the steps taken

```commandline
Laris@Larisha MINGW64 ~ (main)
$ cd

Laris@Larisha MINGW64 ~ (main)
$ pwd
/c/Users/Laris

Laris@Larisha MINGW64 ~ (main)
$ cd .ssh
bash: cd: .ssh: No such file or directory

Laris@Larisha MINGW64 ~ (main)
$ mkdir .ssh

Laris@Larisha MINGW64 ~ (main)
$ cd .ssh

Laris@Larisha MINGW64 ~/.ssh (main)
$ pwd
/c/Users/Laris/.ssh

Laris@Larisha MINGW64 ~/.ssh (main)
$ ssh-keygen -t rsa -b 4096 -C "larisha.as@gmail.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Laris/.ssh/id_rsa): tech241-larisha-az-key
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in tech241-larisha-az-key
Your public key has been saved in tech241-larisha-az-key.pub
The key fingerprint is:
SHA256:4dT/Y1mJLkV73fMFL4JmHcC9PZOyvn0Tjyi9vMbbyLU larisha.as@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
|         ...     |
|         ....    |
|        o . .+.. |
|       o . ++.Bo+|
|        S + +*.**|
|         o  +o.=+|
|           = o*.+|
|          .oB*.+o|
|           oO=E..|
+----[SHA256]-----+

Laris@Larisha MINGW64 ~/.ssh (main)
$ ls
tech241-larisha-az-key  tech241-larisha-az-key.pub

Laris@Larisha MINGW64 ~/.ssh (main)
$ cat tech241-larisha-az-key.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQC6T9PJ1k0oce/Zmb5WBRE9SveaM7E/0rDdF8H5Mrm3bd4nSTvwls/zZaaXwqzyjeg4VlF66kDydd94BhFLuPWxvqzAu9boTG63xaB0fQhexe7KbZFfwAj1pro1zLo3g5Dh7sVt7f2rZ9LYw5qEnCjvWrdCqTLPGitI2jlC+Ch2zVKP/qelR8+c9qLNa4AtT+Ct1wU/hi0BSWEceMpCZ2eTOQZma/BqI4XYmPocMWQvHH4SqglirtTgSCPYtwLV2UNbrG2QeaY7B3WeYQAVt4yPLvAd/e70Lid+3QsV1WrKGwIAdUi8ZC0fiSOI9CYORPVRYLffByvKadEZlrQmhhez3heSw+K7BXY6Jjhnm+tgUetA83CftZss+3ii8gDV3KruEe31HjebmD36byytII+itFd/PZXHQm08AfAnwd8GmXAM5U6WUhZGSiciWBmPab467XY66zDQLhYsyVCU/7iNE8NRtFuZHzC4IVTaMHk0XSvn0TFqfRiU3ryPC9fb6ZywfHx8AyrADQU5AS0cDypo/Ruhl33o818nmssQATyj9Mq9JwrSr3U2wJpOCHme7FOS/MCnbpyYmf2vwbbcVvQdJAxjNUeWe4pwyBX0ScBDkIbN01R5WiUlL/+tzwxnAI64WM+fYnOgsAtWZCxGTBiKt2imX2clpdCHCwpzcd++1Q== larisha.as@gmail.com

Laris@Larisha MINGW64 ~/.ssh (main)
$ chmod 400 tech-larisha-az-key
chmod: cannot access 'tech-larisha-az-key': No such file or directory

Laris@Larisha MINGW64 ~/.ssh (main)
$ chmod 400 tech-larisha-az-key
chmod: cannot access 'tech-larisha-az-key': No such file or directory

Laris@Larisha MINGW64 ~/.ssh (main)
$ ls
tech241-larisha-az-key  tech241-larisha-az-key.pub

Laris@Larisha MINGW64 ~/.ssh (main)
$ chmod 400 tech241-larisha-az-key

Laris@Larisha MINGW64 ~/.ssh (main)
$ ls
tech241-larisha-az-key  tech241-larisha-az-key.pub

Laris@Larisha MINGW64 ~/.ssh (main)
$ ls -1
tech241-larisha-az-key
tech241-larisha-az-key.pub

Laris@Larisha MINGW64 ~/.ssh (main)
$ ls -l
total 8
-r--r--r-- 1 Laris 197121 3389 Jun 20 15:47 tech241-larisha-az-key
-rw-r--r-- 1 Laris 197121  746 Jun 20 15:47 tech241-larisha-az-key.pub

Laris@Larisha MINGW64 ~/.ssh (main)
$ ssh -i ~/.ssh/tech241-larisha-az-key adminuser@20.58.17.81
The authenticity of host '20.58.17.81 (20.58.17.81)' can't be established.
ED25519 key fingerprint is SHA256:Bcpb6cj1Z3Yl1L1KsZgoyy/zKLL+5DKkJuj1JRUUj8k.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '20.58.17.81' (ED25519) to the list of known hosts.
Connection closed by 20.58.17.81 port 22

Laris@Larisha MINGW64 ~/.ssh (main)
$ ssh -i ~/.ssh/tech241-larisha-az-key adminuser@20.58.17.81
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 5.4.0-1108-azure x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Tue Jun 20 15:45:53 UTC 2023

  System load:  0.0               Processes:           100
  Usage of /:   5.6% of 28.89GB   Users logged in:     0
  Memory usage: 26%               IP address for eth0: 10.0.1.16
  Swap usage:   0%

Expanded Security Maintenance for Infrastructure is not enabled.

45 updates can be applied immediately.
32 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

27 additional security updates can be applied with ESM Infra.
Learn more about enabling ESM Infra service for Ubuntu 18.04 at
https://ubuntu.com/18-04



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

adminuser@tech241-larisha-man-app:~$ ls
adminuser@tech241-larisha-man-app:~$ ls -a
.  ..  .bash_logout  .bashrc  .cache  .gnupg  .profile  .ssh
adminuser@tech241-larisha-man-app:~$ exit
logout
Connection to 20.58.17.81 closed.

Laris@Larisha MINGW64 ~/.ssh (main)
$
```commandline
