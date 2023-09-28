# AWS Control Tower SecurityHub Enabler

## Overview

The AWS Control Tower SecurityHub Enabler is an AWS CloudFormation template designed to simplify the process of enabling and configuring AWS Security Hub in the security account of an AWS Control Tower environment. This template creates essential AWS resources, such as IAM roles, Lambda functions, and SNS topics, to automate the Security Hub setup based on your specified parameters.

## Prerequisites

Before you proceed, ensure that you have the following prerequisites in place:

1. **AWS Control Tower Environment**: You must have an AWS Control Tower environment set up.

2. **AWS Access**: You should have AWS CLI or AWS Management Console access with sufficient permissions to deploy CloudFormation templates.

3. **Security Account**: Know the AWS account ID of your Security Account.
