
# Setting Up and Securing an Azure Environment


## Objective:

This project demonstrates the setup, security implementation, and monitoring of an Azure environment. It covers the creation and configuration of essential Azure resources, focusing on establishing a secure and efficient cloud infrastructure. Key steps include setting up a resource group, virtual network, and subnet, configuring network security with specific rules, and deploying a secured Windows Virtual Machine. The project also involves establishing user roles and permissions, integrating Microsoft Defender for Cloud for enhanced security capabilities, and enforcing storage account security through policies.

## Tools and Technologies

- Microsoft Azure
- Azure Portal
- Microsoft Defender for cloud
- Azure Active Directory
- Azure Virtual Machines       
## Project Implementation Steps

### 1. Building the Infrastructure

#### Step 1: Creating a Resource Group

- Action: Created a resource group 'az-test' in Azure to manage all resources for this project.
- Purpose: Organizes all the Azure assets within this project under a unified management scope.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/52d562d6a601f7e84aee57c5df0cf00ee5dfc571/Screenshots/1.%20Create%20resource%20group.png)


#### Step 2: Setting Up a Virtual Network
- Action: Configured the virtual network 'az-vnet' with the address space 10.0.0.0/16.
- Purpose: Provides a private network environment in the cloud for Azure resources to securely communicate with each other.
- - ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/2.%20Create%20VNET.png)
    
#### Step 3: Adding a Subnet
- Action: Created a subnet within 'az-vnet' with an address range of 10.0.0.0/24.
- Purpose: Subdivides the virtual network for more organized and secure resource allocation.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/2.1%20Create%20SUBNET.png)
  
### 2. Enhancing Network Security
#### Step 4: Network Security Group Configuration
- Action: Established 'az-NSG' and defined inbound and outbound security rules for SSH, RDP, and HTTP.
- Purpose: Controls inbound and outbound network traffic to and from Azure resources in the virtual network.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/2.2.%20Create%20NSG.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/2.2.1%20Create%20NSG%20inbound.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/2.2.2%20Create%20NSG%20outbound.png)
  
####  Step 5: Deploying a Virtual Machine
- Action: Launched a Windows Virtual Machine (az-VM) and associated it with 'az-vnet' and 'az-NSG'.
- Purpose: Hosts applications and serves as a central point for managing IT services.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/3.%20Created%20VM.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/3.1%20Created%20VM.png)
  
### 3. Managing Access and Roles
#### Step 6: Setting Up Users and Groups
- Action: Created users like CEO, HR Coordinator, IT Admin, and groups like HR, IT Department, and established roles and permissions.
- Purpose: Manages access and authority within the Azure environment ensuring security and operational efficiency.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/4.1%20Created%20Users.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/4.2%20Created%20GROUPS%20in%20AAD.png)
  
#### Step 7: Configuring Microsoft Defender for Cloud
- Action: Enabled and explored security capabilities in Microsoft Defender for Cloud.
- Purpose: Strengthens the security posture of your data centers, and provides advanced threat protection.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/5.%20Azure%20security%20Centre.png)
  
### 4. Implementing and Monitoring Security Policies
#### Step 8: Enforcing a Secure Transfer Policy
- Action: Created a custom policy to enforce HTTPS transfer for storage accounts.
- Purpose: Ensures that all data transfer to the storage account is over a secure channel.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/6.%20Customize%20security%20policy.png)
- ![App Screenshot]()
  
#### Step 9: Simulating a Policy Violation
- Action: Created 'aztestingstorageaccount' with secure transfer disabled to simulate policy violation and then use Microsoft Defender for cloud to remediate the issue.
- Purpose: To validate the effectiveness of the security policy in identifying non-compliant resources and use recommendations from Mircosoft Defender in order to remediate the no-compliance.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/6.1%20SECURE%20TRANSFER%20DATA%20IS%20SET%20TO%20not%20enabled.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/6.2%20NON-COMPLIANCE%20Error.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/6.3%20Recommendations.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/6.3.1%20Recommendatio%20to%20remediate.png)
  
### 5. Secure Data Storage and Handling
#### Step 10: Setting Up a Secure Storage Account
- Action: Configured 'az-storageaccount001' with "Secure transfer required" enabled.
- Purpose: Guarantees the protection of data in transit to and from Azure storage.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/7.%20Created%20Storage%20account.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/7.1%20Secure%20Data%20Transfer%20is%20ENABLED.png)
  
#### Step 11: Blob Storage and SAS Configuration
- Action: Created az-container in blob storage and uploaded data securely. Configured a SAS token for time-limited and permission-based access.
- Purpose: Provides a secure way to store and access large amounts of unstructured data.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/7.2%20Upload%20data%20to%20blob%20securely.png)  
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/7.3%20Generate%20SAS%20token.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/7.3.1%20Generate%20SAS%20Token.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/7.3.2%20Generate%20SAS%20token.png)
  
### 6. Monitoring the Virtual Machine
#### Step 12: Creating a Log Analytics Workspace
- Action: Developed 'az-LogAnalytics' for centralized logging and monitoring of 'az-VM'.
- Purpose: Collects and analyzes data generated by resources in your Azure and on-premises environments.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/8.1.1%20Create%20workspace%20for%20Log%20Analytics%20worspace%20for%20azure%20monitor%20.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/8.1.2%20Workspace%20ID%20and%20Key.png)
  
#### Step 13: Setting Up VM Monitoring
- Action: Installed Log Analytics agent on 'az-VM' and set up performance counters and alert rules.
- Purpose: To monitor the health and performance of the VM, ensuring timely alerts for potential issues.
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/8.1.3.3%20Succesfully%20installed%20MOM%20on%20VM.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/8.1.4%20Configure%20Data%20collection%20.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/8.1.5%20View%20Data%20in%20Metrics.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/8.1.5.1.%20Create%20alert%20rule.png)
- ![App Screenshot](https://github.com/SarthakRana007/Azure-Security-Project/blob/d5d6bc2d9da8550cad3ccb4cc0c17132418a3e95/Screenshots/8.1.5.2.%20Set%20notification%20for%20alert%20rule.png)
  
## Security Considerations and Mitigation Strategies

At the conclusion of this project, it's crucial to understand the potential security threats that an Azure environment can face and the ways our configuration helps mitigate them:

- Network Security: By setting up NSGs (Network Security Groups), we've established a barrier against unauthorized network access, effectively safeguarding our virtual network and VM.

- Data Encryption: Enforcing the "Secure transfer required" policy ensures that all data transmitted to and from Azure storage is encrypted, preventing data interception and leakage.

- Access Management: Through Azure Active Directory and role-based access control (RBAC), we've ensured that only authorized personnel have access to specific Azure resources, reducing the risk of internal threats.

- Monitoring and Compliance: Utilizing Azure Security Center and Log Analytics helps us monitor the security state of our services, detect threats, and ensure compliance with security policies.

- Resilient Infrastructure: By configuring our virtual machines and storage accounts with redundancy and backup protocols, we've built resilience against data loss and service interruptions.

This project's approach to building a secure Azure environment provides a foundational understanding of cloud security best practices and prepares for advanced security implementations and threat handling in cloud-based infrastructures.
