# Commands to install Terraform on Ubuntu

```bash
wget https://releases.hashicorp.com/terraform/1.8.0/terraform_1.8.0_linux_amd64.zip
# change the version to whichever you wish

unzip terraform_1.8.0_linux_amd64.zip
 
sudo mv terraform /usr/local/bin
```



Sure! Here’s a similar set of commands for managing Terraform on Ubuntu.

---

# Commands to Install Terraform on Ubuntu

```bash
# Install the required dependencies
sudo apt update
sudo apt install -y wget unzip

# Download Terraform binary
wget https://releases.hashicorp.com/terraform/1.5.6/terraform_1.5.6_linux_amd64.zip

# Unzip the downloaded file
unzip terraform_1.5.6_linux_amd64.zip

# Move the binary to a directory included in your system’s PATH
sudo mv terraform /usr/local/bin/

# Verify the installation
terraform --version
```

# Basic Terraform Commands

## INIT & APPLY

```bash
# Initialize a Terraform configuration directory
terraform init

# Validate the configuration files
terraform validate

# Format Terraform configuration files
terraform fmt

# Create an execution plan (shows what Terraform will do)
terraform plan

# Apply the changes required to reach the desired state of the configuration
terraform apply

# Destroy the resources managed by Terraform
terraform destroy
```

## STATE MANAGEMENT

```bash
# Show the current state of the Terraform-managed infrastructure
terraform show

# List the resources in the state
terraform state list

# Remove a resource from the state
terraform state rm <resource_address>

# Move an item in the state
terraform state mv <source> <destination>
```

## MODULES

```bash
# Get and install modules defined in the configuration
terraform get

# List available modules
terraform modules
```

## PROVIDERS & VARIABLES

```bash
# List the providers required by the configuration
terraform providers

# Set or change variables for the configuration
terraform variables
```

## WORKSPACE MANAGEMENT

```bash
# Create a new workspace
terraform workspace new <workspace_name>

# Select a workspace to work in
terraform workspace select <workspace_name>

# List all workspaces
terraform workspace list

# Delete a workspace
terraform workspace delete <workspace_name>
```

## MODULE REGISTRY

```bash
# Search for modules in the Terraform Registry
terraform search <module_name>

# Get detailed information about a specific module
terraform module-info <module_name>
```
