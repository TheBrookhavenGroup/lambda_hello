# lambda_hello
Learning how to use Terraform to deploy an AWS python lambda service

Basic idea is to create a `main.tf` terraform config file.  Run terraform and it builds and deploys.  That tf file specify deployment by zip file which happens under the hood.


## Tutorial

https://www.middlewareinventory.com/blog/aws-lambda-terraform/

## Steps

Install aws cli https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html#getting-started-install-instructions

Get an AWS Access Key ID and Secret.

Run `$ aws configure`

Install Terraform
Reference: https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli

That reference also has a quick start tutorial to use Docker to provision Nginx in less than a minute.

```bash
$ brew tap hashicorp/tap
$ brew install hashicorp/tap/terraform
$ brew update
$ brew upgrade hashicorp/tap/terraform
$ touch ~/.zshrc (or .bashrc)
$ terraform -install-autocomplete
```

## Initialize and Run Terraform

```bash
$ terraform init
$ terraform plan -out tfplan.out
$ terraform apply tfplan.out
```

Now the [aws lambda console](https://us-east-1.console.aws.amazon.com/lambda/home?region=us-east-1#/functions) should list the lambda function "welcome".