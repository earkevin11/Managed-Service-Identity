# Managed-Service-Identity

# What is a Managed Identity?
- Application object can be used as an identity for applications to access Azure resources.
- Managed Identity can be enabled in the Azure VM where an identity will be created in Azure AD.
- Then you can give access to the Managed Identity to access Azure Resources


# How to create the managed identity?
- Key Vault > Identity > Enable Managed Identity

# Add the access policy and configure permissions for the managed identity
- Select principal > select the managed identity 


# Use Case
- Create the managed identity for the virtual machine so that the VM can get the keys within the key vault.
