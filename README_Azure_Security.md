
# Setting Up and Securing an Azure Environment


## Objective:

This project demonstrates the setup, security implementation, and monitoring of an Azure environment. It covers the creation and configuration of essential Azure resources, focusing on establishing a secure and efficient cloud infrastructure. Key steps include setting up a resource group, virtual network, and subnet, configuring network security with specific rules, and deploying a secured Windows Virtual Machine. The project also involves establishing user roles and permissions, integrating Microsoft Defender for Cloud for enhanced security capabilities, and enforcing storage account security through policies.

## Tools and Technologies

- Microsoft Azure
- Azure Portal
- Azure Security Center
- Azure Active Directory
- Azure Virtual Machines       
## Project Implementation Steps

### 1. Building the Infrastructure

#### Step 1: Creating a Resource Group

- Action: Created a resource group az-test in Azure to manage all resources for this project.
- Purpose: Organizes all the Azure assets within this project under a unified management scope.

#### Step 2: Setting Up a Virtual Network
- Action: Configured the virtual network az-vnet with the address space 10.0.0.0/16.
- Purpose: Provides a private network environment in the cloud for Azure resources to securely communicate with each other.
#### Step 3: Adding a Subnet
- Action: Created a subnet within az-vnet with an address range of 10.0.0.0/24.
- Purpose: Subdivides the virtual network for more organized and secure resource allocation.
### 2. Enhancing Network Security
#### Step 4: Network Security Group Configuration
- Action: Established az-NSG and defined inbound and outbound security rules for SSH, RDP, and HTTP.
- Purpose: Controls inbound and outbound network traffic to and from Azure resources in the virtual network.
####  Step 5: Deploying a Virtual Machine
- Action: Launched a Windows Virtual Machine (az-VM) and associated it with az-vnet and az-NSG.
- Purpose: Hosts applications and serves as a central point for managing IT services.
### 3. Managing Access and Roles
#### Step 6: Setting Up Users and Groups
- Action: Created users like CEO, HR Coordinator, IT Admin, and groups like HR, IT Department, and established roles and permissions.
- Purpose: Manages access and authority within the Azure environment ensuring security and operational efficiency.
#### Step 7: Configuring Microsoft Defender for Cloud
- Action: Enabled and explored security capabilities in Microsoft Defender for Cloud.
- Purpose: Strengthens the security posture of your data centers, and provides advanced threat protection.
### 4. Implementing and Monitoring Security Policies
#### Step 8: Enforcing a Secure Transfer Policy
- Action: Created a custom policy to enforce HTTPS transfer for storage accounts.
- Purpose: Ensures that all data transfer to the storage account is over a secure channel.
#### Step 9: Simulating a Policy Violation
- Action: Created aztestingstorageaccount with secure transfer disabled to simulate policy violation.
- Purpose: To validate the effectiveness of the security policy in identifying non-compliant resources.
### 5. Secure Data Storage and Handling
#### Step 10: Setting Up a Secure Storage Account
- Action: Configured az-storageaccount001 with "Secure transfer required" enabled.
- Purpose: Guarantees the protection of data in transit to and from Azure storage.
#### Step 11: Blob Storage and SAS Configuration
- Action: Created az-container in blob storage and uploaded data securely. Configured a SAS token for time-limited and permission-based access.
- Purpose: Provides a secure way to store and access large amounts of unstructured data.
### 6. Monitoring the Virtual Machine
#### Step 12: Creating a Log Analytics Workspace
- Action: Developed az-LogAnalytics for centralized logging and monitoring of az-VM.
- Purpose: Collects and analyzes data generated by resources in your Azure and on-premises environments.

#### Step 13: Setting Up VM Monitoring
- Action: Installed Log Analytics agent on az-VM and set up performance counters and alert rules.
- Purpose: To monitor the health and performance of the VM, ensuring timely alerts for potential issues.

## Security Considerations and Mitigation Strategies

At the conclusion of this project, it's crucial to understand the potential security threats that an Azure environment can face and the ways our configuration helps mitigate them:

- Network Security: By setting up NSGs (Network Security Groups), we've established a barrier against unauthorized network access, effectively safeguarding our virtual network and VM.

- Data Encryption: Enforcing the "Secure transfer required" policy ensures that all data transmitted to and from Azure storage is encrypted, preventing data interception and leakage.

- Access Management: Through Azure Active Directory and role-based access control (RBAC), we've ensured that only authorized personnel have access to specific Azure resources, reducing the risk of internal threats.

- Monitoring and Compliance: Utilizing Azure Security Center and Log Analytics helps us monitor the security state of our services, detect threats, and ensure compliance with security policies.

- Resilient Infrastructure: By configuring our virtual machines and storage accounts with redundancy and backup protocols, we've built resilience against data loss and service interruptions.

This project's approach to building a secure Azure environment provides a foundational understanding of cloud security best practices and prepares for advanced security implementations and threat handling in cloud-based infrastructures.