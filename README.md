## Installing Terraform
- get gpg keys to identify the hashicorp developers who maintain the repo
wget -O - https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg

- add repo to list of package repositories
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

- update repositories and install Terraform
sudo apt update && sudo apt install terraform

## Generating SSH keys
ssh-keygen -t ed25519 -f .ssh/do-key

## Terraform Commands

### 1. Initialize the Configuration
```bash
terraform init
```

### 2. Format the Configuration
```bash
terraform fmt
```

### 3. Plan the Infrastructure
```bash
terraform plan
```

This command will show you what resources Terraform intends to create, modify, or destroy.

### 4. Apply the Configuration
```bash
terraform apply
```
