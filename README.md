# Managed-Service-Identity

# What is a Managed Identity? #240
- Application object can be used as an identity for applications to access Azure resources.
- Managed Identity can be created in the Azure VM.
- Then you can give access via RBAC to the Managed Identity to access Azure Resources

# What problem does a Managed Service identity solve? 
- MSI eliminates the need for developers to manage credentials.
- Developers have a hard time managing credentials and MSI automates it.
- Oftentimes we will see a managed identity used by the application to obtain an access token or a refresh token

# What are the two types of managed service identitiy?
- System-managed identity
- User-assigned managed identitiy

# System-managed identities 
- System-managed identities have a 1:1 relationship with Azure resources.
- It is created along with the Azure resource (You must enable the system-managed identity when creating the Azure resource)
- If you delete the managed identity, the Azure resource is also deleted.

# User-assigned managed identities
- User-assigned managed identities are independent of the Azure resources.
- Can stand alone and be given to multiple resources.
- It is not tied to Azure resources. If users delete the user-assigned managed identity, the Azure resource will not be deleted.

# Excellent metaphor/diagram describing Managed Identities
- System-Managed Identities
- User-Assigned Managed Identities

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/194352603-2d3e545a-8712-410e-be41-78caf6ba2761.png" height="85%" width="85%" alt="Privileged Identity Management"/>

<p/>


# How to create the managed identity?
- Key Vault > Identity > Enable Managed Identity

# Add the access policy and configure permissions for the managed identity
- Select principal > select the managed identity 


# Use Case
- Create the managed identity for the virtual machine so that the VM can get the keys within the key vault.




# Difference between Application Object vs Service Principal vs Managed Identity
- Application Object - the application links to the application object and that is how the app can get access to Azure resources
- Managed Identity - is used for <str> Azure resources only </str> such as Azure VM. The identity is managed by Azure.
- Service principal - the service principal is created when an managed identity/app object is created.
- Service principal is assigned access to Azure resources for the managed identity and app object.
- The service principal is what is given access to resources on the Azure platform.
