# Terraform EKS Cluster Setup

## Project Layout
```
eks-terraform/
├─ provider.tf
├─ variables.tf
├─ vpc.tf
├─ iam.tf
├─ eks.tf
├─ node_group.tf
├─ outputs.tf
```

## provider.tf
```hcl
terraform {
  required_version = ">= 1.0"
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = ">= 4.0"
    }
  }
}
provider "aws" {
  region = var.aws_region
}
```

## variables.tf
(Full variables content from previous message…)

## vpc.tf
(Full vpc.tf content…)

## iam.tf
(Full iam.tf content…)

## eks.tf
(Full eks.tf content…)

## node_group.tf
(Full node_group.tf content…)

## outputs.tf
(Full outputs.tf content…)

## How to Apply
```bash
terraform init
terraform plan
terraform apply
aws eks update-kubeconfig --region <region> --name <cluster_name>
kubectl get nodes
```
