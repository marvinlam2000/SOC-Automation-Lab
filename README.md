# SOC-Automation-Lab

## Objective
Creating a Security Operations Center (SOC) automation project (home lab) on the cloud. Goal is to explore how automation enhances incident response, accelerates threat detection, and streamlines SOC workflows.

### Skills Learned
- Creating diagrams to visualize how processes work and how information is being processed.
- 
### Tools Used
<img src="https://img.shields.io/badge/-Draw.io-F08705?&style=for-the-badge&logo=diagramsdotnet&logoColor=white" /><img src="https://img.shields.io/badge/-VirtualBox-183A61?&style=for-the-badge&logo=virtualbox&logoColor=white" /><img src="https://img.shields.io/badge/-Sysmon-8A2BE2?&style=for-the-badge&logo=windows&logoColor=white" /><img src="https://img.shields.io/badge/-Wazuh-5A9EC9?&style=for-the-badge&logo=wazuh&logoColor=white" /><img src="https://img.shields.io/badge/-TheHive-FADA5E?&style=for-the-badge&logo=TheHive&logoColor=black" /><img src="https://img.shields.io/badge/-DigitalOcean-0080FF?&style=for-the-badge&logo=digitalocean&logoColor=white" />


## Steps
Step 1. Create a diagram of the process on draw.io. Helps user to visualize the process while working on the project.![SOCdiagram](https://github.com/user-attachments/assets/9c51927a-0431-4157-8fca-3068876a24b0)

Step 2. Download Virtual Box and Create a VM with Window's 10 iso image file. Proceed to the Virtual Machine and download Sysmon on the VM. 
![step 2](https://github.com/user-attachments/assets/4b8b33c7-1560-4156-88bb-6c7ff58640e1)

Step 3. On virtual machine create an account with digital ocean and create a Digital Ocean droplet. Create a firewall and specify rules and modify inbound traffic to users Virtual Machine IP. 
![step 3a](https://github.com/user-attachments/assets/f7cf1162-6230-4f6e-967f-c04dbb821377)
![step 3b](https://github.com/user-attachments/assets/cb79e9d6-601c-4ff2-b35f-59ef26009a4d)

Step 4. Download and install Wazuh. Use ssh on putty to perfom the installation process. Use a secure connection method to login to droplet's IP address in a new tab.
![step 4a](https://github.com/user-attachments/assets/3bc4eaed-554f-4ef2-a871-cbf43dab3de4)
![step 4b](https://github.com/user-attachments/assets/bfa08996-de4f-4379-9d0a-437280a329a4)

Step 5. Create a new droplet and make sure the firewall created earlier is connected to the droplet the user just created. The droplet I created is "thehive". Installed Java, Cassandra, ElasticSearch, and theHive in putty.
![step 5a](https://github.com/user-attachments/assets/39581a8d-5e85-41ca-bf63-938fcaa6ac25)
![Step 5b](https://github.com/user-attachments/assets/429d12df-885a-4927-bf69-43c2f86642a8)


