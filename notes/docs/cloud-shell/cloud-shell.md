# Description
- A command-line environment you can access through your web browser to manage Azure resources
- Authenticated, interactive shell that isn't part of a local machine
- Also provides cloud storage to persist files such as SSH keys, scripts, and more. This functionality lets you access important files in between sessions and with different machines. 
- Use the Cloud Shell editor to make changes to files, such as scripts, that are saved into this cloud storage directly from the Cloud Shell interface

# Access
- [https://shell.azure.com](https://shell.azure.com)
- From the Azure portal
- In Microsoft Learn

# How it works
- When you open a Cloud Shell session, a temporary host (VM) is allocated to your session.
- You can select either PowerShell or Bash to use
- Cloud Shell sessions terminate after 20 minutes of inactivity. 

# File Operations
- When a session terminates, files on your CloudDrive are persisted.
- You can persist files on Cloud Shell by using the Azure CloudDrive
- After uploading files, you can interact with them as you would in a regular PowerShell or Bash session
- Cloud Shell also lets you map an Azure Storage File Share, which is tied to a specific region.
- If you need to edit scripts hosted on the CloudDrive or File Share, you can use the Cloud Shell editor or by entering `code` in the terminal

# Tooling
- If you need to manage resources (such as Docker containers or Kubernetes Clusters) or want to use non-Microsoft tools (such as Ansible and Terraform) in Cloud Shell, the Cloud Shell session comes with these add-ons already preconfigured.

# When to use it
- Work from anywhere (any browser-based device)
- Reduce the need to install plug-ins or add-ons to your device
- Session-based work (edit and persist files between sessions for later use)

# When not to use it
- When working in sessions for more than 20 minutes or for long running scripts or activities
- When in need of admin permissions, such as sudo acess
- When in need of installing tools that arenÄt supported by Cloud Shell
- When in need of storage from a different regions. You might need to back up and synchronize this content since only one region can have the storage allocated to Azure Cloud Shell.
- When in need of opening multiple sessions at the same time. Azure Cloud Shell allows only one instance at time and isn't suitable for concurrent work across multiple subscriptions or tenants.