# GH ARC K8s Instance

Provisions an ubuntu ec2 instance with the following installed/configured:
* aws cli, helm, kubectl (with Autocomplete)
* kind (k8s cluster)
* Github Action Runner Controller

Note:
* By default, uses a custom actions-runner image (patrickameh/action-runner:0.0.1) - which adds curl to GH actions runner image
* By default, targets default vpc in an AWS account (change in main.tf line 65 if desired)

Required (Non-defaulted) Variables:
* github_config_url
* github_token

To execute:
* Install Terraform
* Configure AWS Credentials/Profile
* Navigate into this directory
* Set AWS Credentials/Profile (e.g. export AWS_PROFILE=myprofilename)
* Set values for variables in variables.tf as desired
* Run Terraform Init and Terraform Apply