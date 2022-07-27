# Managed-Service-Identity

# What is a Managed Identity? #240
- Application object can be used as an identity for applications to access Azure resources.
- Managed Identity can be enabled in the Azure VM where an identity will be created in Azure AD.
- Then you can give access to the Managed Identity to access Azure Resources


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
