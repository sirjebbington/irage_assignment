# irage_assignment
Assignment given by Irage.  
Scenario: 
You’ve joined a team that needs to manage two isolated environments: staging and production. Your task is to create a production-grade Terraform setup that adheres to best practices, includes separation of concerns, security, and works with a GitOps workflow. 
✅ What You Must Do 
1. Design a Terraform Architecture 
  ● Use modular design (no copy-paste between envs) 
  ● Support both staging and production via: 
  ○ terraform.tfvars or workspace logic 
  ● Use backend config with S3 and DynamoDB 
2. Provision the Following AWS Resources 
  ● 1 VPC per environment 
  ● 2 subnets per VPC (public + private) 
  ● 1 EC2 bastion host in public subnet 
  ● 1 RDS instance in private subnet (Postgres/MySQL) 
  ● 1 security group for bastion and RDS 
  ● RDS should not be publicly accessible 
  ● Bastion host should only allow SSH from user’s IP 
  ● Use user data to bootstrap bastion
3. Include GitOps CI Workflow (e.g., GitHub Actions) ● When a PR is raised: 
  ○ Run terraform fmt, validate, and plan 
  ● On merge to main, apply to staging 
  ● On tag v*.*.*, apply to production 
4. Provide Documentation 
  ● Project structure explanation 
  ● Decisions made (module design, variable handling, secrets, etc.) ● Manual testing instructions 
  ● Environment switching explanation
