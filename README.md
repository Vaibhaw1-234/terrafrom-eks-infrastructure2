# terrafrom-eks-infrastructure2
2. Configure AWS Credentials
To authenticate with AWS, you need to provide AWS credentials. You can do this securely by storing your AWS credentials as GitHub Secrets.

Go to your GitHub repository on GitHub.
Click on "Settings" -> "Secrets and variables" -> "Actions".
Click on "New repository secret" and add the following secrets:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
The GitHub Actions workflow will use these secrets to authenticate with AWS.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

4. Push Changes and Trigger Workflow
Once you have created the workflow file and set up the secrets, you need to push your changes to the repository.

Commit and push the workflow file to the main branch:
sh
Copy code
git add .github/workflows/terraform-provision.yml
git commit -m "Add GitHub Actions workflow for Terraform"
git push origin main
Make a change in your Terraform code or configuration and push it to the main branch. This will trigger the GitHub Actions workflow and provision/update the infrastructure as per the changes.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------
Summary of GitHub Actions Workflow
Checkout Code: Retrieves the latest code from the repository.
Set up Terraform: Installs the specified Terraform version.
Terraform Init: Initializes Terraform and downloads required providers.
Terraform Plan: Creates a plan for the changes to be made.
Terraform Apply: Applies the changes automatically if the event is a push to the main branch.
Terraform Output: Displays the output values from the Terraform ru






