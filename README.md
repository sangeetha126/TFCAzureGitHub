Here’s a basic example of a Terraform Cloud workflow using Azure and GitHub. This setup assumes:

You store your Terraform code in a GitHub repo.
You use Terraform Cloud for remote state and runs.
You want to provision Azure resources.
1. Terraform Cloud Setup

Create a workspace in Terraform Cloud.
Connect it to your GitHub repo.
Set the following environment variables in the workspace (mark sensitive as needed):
ARM_CLIENT_ID
ARM_CLIENT_SECRET
ARM_SUBSCRIPTION_ID
ARM_TENANT_ID

Notes:

For security, do not store secrets in .env or code. Use GitHub Actions secrets and Terraform Cloud workspace variables.
The workflow above only plans by default. Uncomment Terraform Apply to enable automatic applies.
Adjust organization/workspace names as needed.