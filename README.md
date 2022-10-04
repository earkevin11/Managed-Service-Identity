# Managed-Service-Identity

# What is a Managed Identity? #240
- Application object can be used as an identity for applications to access Azure resources.
- Managed Identity can be enabled in the Azure VM where an identity will be created in Azure AD.
- Then you can give access to the Managed Identity to access Azure Resources

# What problem does a Managed Service identity solve? 
- MSI eliminates the need for developers to manage credentials.
- Developers have a hard time managing credentials and MSI automates it.


# What are the two types of managed service identitiy?
- System-managed identity
- User-assigned managed identitiy

# System-managed identities 
- System-managed identities have a 1:1 relationship with Azure resources.
- It is created along with the Azure resource.
- If you delete the managed identity, the Azure resource is also deleted.

# User-assigned managed identities
- User-assigned managed identities are independent of the Azure resources.
- Can stand alone and be given to multiple resources.
- It is not tied to Azure resources. Delete managed identity and resource will not be deleted.


# How to create the managed identity?
- Key Vault > Identity > Enable Managed Identity

# Add the access policy and configure permissions for the managed identity
- Select principal > select the managed identity 


# Use Case
- Create the managed identity for the virtual machine so that the VM can get the keys within the key vault.




# Difference between Application Object vs Service Principal vs Managed Identity
- Application Object - application links to application object where the app can now get access to Azure resources
- Managed Identity - is used for Azure resources only such as Azure VM. The identity is managed by Azure.
- Service principal - the service principal is created when an managed identity/app object is created.
- Service principal is assigned access to Azure resources for the managed identity and app object.
