# Create an EC2 instance using Python

This Python script uses the `boto3` library to launch an EC2 instance on Amazon Web Services (AWS) and retrieve the instance's information, including its public and private IP addresses.

## Prerequisites

Before running this script, ensure that the following prerequisites are met:

1. **AWS Account**: You need an active AWS account.
2. **IAM User with Permissions**: Make sure you have an AWS IAM user with the necessary permissions to create and manage EC2 instances.
3. **AWS CLI configured**: The script relies on `boto3`, which uses your local AWS CLI configuration. Make sure to run `aws configure` and provide your AWS Access Key ID, Secret Access Key, default region, and output format.
4. **Key Pair**: You need a key pair to be specified in `key_name` for connecting to the instance later.
5. **Security Group**: Ensure you have a security group ID that allows the necessary traffic (e.g., SSH, HTTP).

## Features

- Launches an EC2 instance with the following parameters:
  - **Image ID**: Set by `image_id` (e.g., `ami-0557a15b87f6559cf` for Amazon Linux).
  - **Instance Type**: Set to `t2.micro` (eligible for free tier).
  - **Key Pair**: The script uses the key pair specified by `key_name` to enable SSH access to the instance.
  - **Security Group**: Associates the instance with a security group to define network access rules.
  - **Subnet**: Places the instance within a specified subnet for proper networking.

## Requirements

- **Python 3.x**
- **boto3**: AWS SDK for Python
  You can install `boto3` using pip:

  ```bash
  pip install boto3
  ```
