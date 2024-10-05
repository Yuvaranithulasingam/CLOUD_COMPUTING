# NETWORKING

## AIM:

To set up a virtualized test environment using VirtualBox, create and configure virtual machines, establish networking, and manage backups, SSH, and FTP connections.

## APPARATUS REQUIRED :

VirtualBox, Operating System (OS), Virtual Machine ISO , SSH Client ,FTP Client, Network Tools.

## THEORY:

In virtualization, a Virtual Machine (VM) emulates a physical computer. VMs provide an isolated environment, allowing different operating systems to run simultaneously on the same hardware. Networking in VMs can be configured using NAT (Network Address Translation) and Bridged Networking modes, allowing access to public or private networks. Key features include port forwarding for remote access and backup mechanisms for VM states.

## PROCEDURE : 

1) Download and Install VirtualBox
2) VM Network Setup:
      </BR>Configure NAT Network:</BR>
              Open VirtualBox > Tools > Network > NAT Networks > Create New.
              Configure IP settings as required for the test environment.
      </BR>Port Forwarding Setup:</BR>
              Navigate to Port Forwarding settings.
              Configure ports for SSH (port 22) and HTTP (port 80) for web access
3) Virtual Machine Setup:
      </BR>Download OS ISO: </BR>
              Download the CentOS Stream 9 ISO file from the CentOS official site.
      </BR>Create Virtual Machine:</BR>
              Open VirtualBox, click New and set up the VM using the CentOS ISO.
              Allocate necessary resources (CPU, RAM, Storage) and proceed with the OS 
              installation.
4) Virtual Machine Network Setup:
      </BR>Bridged Network for Web Server:</BR>
           Ensure the VM is configured with a Bridged Adapter for the web server. This allows 
           public network access.
      </BR>NAT Network for Database Server:</BR>
           Configure the VM with NAT Network for database server isolation, where only the web 
           server host can access it.
5) Virtual Machine Backup & Restore:
     </BR>VM Snapshot:</BR>
           Take a VM snapshot to capture the current state, which can be restored later if 
           needed.
     </BR>VM Clone:</BR>
           Clone the VM for backup or to quickly create a new VM with the same configuration.
6) SSH and FTP Connection Setup:
     </BR>Download Putty: </BR>
           Install Putty for SSH connection.
           Use Putty to connect to the VM by providing the VM’s IP address.
    </BR>Download WinSCP: </BR>
           Install WinSCP for file transfer between host and VM using SFTP.

## VIRTUAL MACHINE CONFIGURATION:

Hostname Setting: Set the hostname using
```
hostnamectl set-hostname <your-name>
```
Confirm the hostname with
```
hostname
```
Open /etc/hostname file to permanently set the hostname.

## IP ADDRESS SETTINGS:
Configure the network settings using nmtui (Text-based interface for network setup):
Edit the connection, configure the IP address, and activate the connection.

Kernel Version:
```
cat /proc/version
```
RAM Information:
```
cat /proc/meminfo
```
Disk Information:
```
df -h
```

## LINUX COMMANDS:

Switch User:
```
su <username>
```
Add User and Password:
```
useradd <new-user>
passwd <new-user>
```
Add a new group:
```
groupadd <new-group>
```
Install Package:
```
yum install <package-name>
```
Update Package:
```
yum update <package-name>
```
Remove Package:
```
yum remove <package-name>
```
### NAME : YUVARANI T
### REGISTER NO : 212222110057

## TEST PAGE:

## RESULT: 
The virtualized test environment was successfully set up with VirtualBox, networking, and IP configurations. SSH and FTP connections were established, and basic system and file management tasks were completed.
