# SOC-Automation-Lab

## Objective
Creating a Security Operations Center (SOC) automation project (home lab) on the cloud. Goal is to explore how automation enhances incident response, accelerates threat detection, and streamlines SOC workflows.

### Skills Learned
- Creating diagrams to visualize how processes work and how information is being processed.
- Creating and configuring firewall rules and attaching firewall to certain servers.
- Configuring theHive and Wazuh through putty.
- Generate Telemetry & Ingest into Wazuh. Sent Telemetry containing Mimikatz. Triggered Mimikatz through Custom Alerts.
- Connect SOAR to send alerts to theHive as well as alerts through email to the analyst.
### Tools Used
<img src="https://img.shields.io/badge/-Draw.io-F08705?&style=for-the-badge&logo=diagramsdotnet&logoColor=white" /><img src="https://img.shields.io/badge/-VirtualBox-183A61?&style=for-the-badge&logo=virtualbox&logoColor=white" /><img src="https://img.shields.io/badge/-Sysmon-8A2BE2?&style=for-the-badge&logo=windows&logoColor=white" /><img src="https://img.shields.io/badge/-Wazuh-5A9EC9?&style=for-the-badge&logo=wazuh&logoColor=white" /><img src="https://img.shields.io/badge/-TheHive-FADA5E?&style=for-the-badge&logo=TheHive&logoColor=black" /><img src="https://img.shields.io/badge/-DigitalOcean-0080FF?&style=for-the-badge&logo=digitalocean&logoColor=white" /><img src="https://img.shields.io/badge/-PuTTY-002147?&style=for-the-badge&logo=putty&logoColor=white" /><img src="https://img.shields.io/badge/-Shuffle-0088CC?&style=for-the-badge&logo=shuffle&logoColor=white" />


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

Step 6. On putty, configure Java, Cassandra, and ElasticSearch to theHive IP address and check each service to see if the service is running. After each service use the systemctl status command to check the status of the service before moving on. 
![Step 6a](https://github.com/user-attachments/assets/cf7482be-a938-4cdf-ac30-7f16c90e259e)
![step 6b](https://github.com/user-attachments/assets/c21357bd-9514-4349-b720-05d03c6c2969)

Step 7. Create an agent on Wazuh and configure on Windows powershell to the IP address of the cloud from DigitalOcean.
![step 7](https://github.com/user-attachments/assets/af1c1795-2448-4890-88a5-8cb697a3e3c7)

Step 8. Go to windows security and create an exclusion before downloading Mimikatz. Be sure to disable protection when downloading the file. Then create an alert on Wazuh for "wazuh archives".
![step 8](https://github.com/user-attachments/assets/1372effd-66b5-4031-81ad-f57219b2eaeb)

Step 9. The file mimikatz is now a part of the alerts. I used Windows powershell to execute the file then Wazuh alerts was able to pick up some mimikatz logs under the "wazuh archives" alerts. 
![step 9](https://github.com/user-attachments/assets/4fe8c518-aeb5-4ece-8349-9d1b98f52d6f)

Step 10. Create an account with Shuffler.io and create a webhook. Integrate the custom webhook into the Wazuh manager and configure the webhook to trigger alerts of ID instead of levels. Make sure to restart the Wazuh manager service everytime there is a change. 
![step 10a](https://github.com/user-attachments/assets/53b6b39f-957f-40d0-b431-cb6e0df17fc0)
![step 10b](https://github.com/user-attachments/assets/4887e9d7-d5b5-4e3a-a462-10e30c9c1192)
![step 10c](https://github.com/user-attachments/assets/457625a8-1dd6-47c0-a040-a39168ae3605)

Step 11. Create an alert on theHive so that the user can connect the alerts received to forward them to an email. It allows the users to filter specifically what they are looking for relating to the alert.
![step 11a](https://github.com/user-attachments/assets/b7ce2783-52b9-46f4-bad7-98e628261b5f)
![step 11b](https://github.com/user-attachments/assets/0a2a7dcd-67e0-47ca-9cd2-c9e796903fee)













