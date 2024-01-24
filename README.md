
# Super Mario Deployment on Kubernetes using Terraform and AWS EKS

## Prerequisites

- AWS account with basic knowledge

- EC2 instance with necessary permissions

- IAM EC2 role for authentication

- Docker, Terraform, AWS CLI, and kubectl installed on the EC2 instance

## Steps

### Step 1: Login and Basics Setup

1\. Login to AWS account as root user.

2\. Launch an EC2 instance with specified settings.

3\. Connect to the instance using SSH.

4\. Run the provided commands to update and install dependencies.

### Step 2: Setup Docker, Terraform, AWS CLI, and Kubectl

1\. Install Docker.

2\. Setup Terraform.

3\. Install AWS CLI.

4\. Setup kubectl.

### Step 3: IAM Role for EC2

1\. Open IAM in the AWS Management Console.

2\. Click on "Roles" and create a new role for EC2.

3\. Choose "AdministratorAccess" permissions.

4\. Complete the role creation process.

### Step 4: Attach IAM Role with Your EC2

1\. Navigate to EC2 instances.

2\. Modify IAM role in the security settings.

3\. Choose the created IAM role from the dropdown and update.

### Step 5: Building Infrastructure Using Terraform

1\. Clone the GitHub repository.

2\. Edit the backend.tf file with your bucket and region.

3\. Run `terraform init`, `terraform validate`, `terraform plan`, and `terraform apply --auto-approve`.

### Step 6: Creation of Deployment and Service for EKS

1\. Change to the EKS-TF directory.

2\. Create the deployment using `kubectl apply -f deployment.yaml`.

3\. Create the service using `kubectl apply -f service.yaml`.

4\. Run `kubectl get all` to check details.

5\. Access the load balancer ingress in a browser.

### Step 7: Destroy All the Infrastructure

1\. Delete deployment and service using `kubectl delete`.

2\. Destroy the infrastructure using `terraform destroy --auto-approve`.

3\. Terminate the EC2 instance after a few minutes.

This project deploys Super Mario on Kubernetes using Terraform and AWS EKS. Ensure to destroy all resources to avoid AWS billing.
