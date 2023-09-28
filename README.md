# AWS Control Tower SecurityHub Enabler

## Overview

The AWS Control Tower SecurityHub Enabler is an AWS CloudFormation template designed to simplify the process of enabling and configuring AWS Security Hub in the security account of an AWS Control Tower environment. This template creates essential AWS resources, such as IAM roles, Lambda functions, and SNS topics, to automate the Security Hub setup based on your specified parameters.

## Prerequisites

Before you proceed, ensure that you have the following prerequisites in place:

1. **AWS Control Tower Environment**: You must have an AWS Control Tower environment set up.

2. **AWS Access**: You should have AWS CLI or AWS Management Console access with sufficient permissions to deploy CloudFormation templates.

3. **Security Account**: Know the AWS account ID of your Security Account.

## Parameters

When deploying this template, you will be prompted to provide the following parameters:

- **SecurityAccountId:** The AWS account ID of the Security Account, which is generally the AWS Control Tower Audit account.

- **ExcludedAccounts:** A comma-separated list of AWS account IDs to be excluded from Security Hub configuration. This can include Management accounts, Log Archive accounts, and Audit accounts.

- **OrganizationId:** The AWS Organizations ID for the Control Tower, used to restrict permissions.

- **RegionFilter:** Specify whether Security Hub should be enabled for all Security Hub supported regions or only Control Tower supported regions.

- **OUFilter:** Specify whether Security Hub should be enabled for all AWS accounts or only accounts in Control Tower Managed Organizational Units (OUs).

- **S3SourceBucket:** The S3 bucket containing the SecurityHubEnabler Lambda deployment package.

- **S3SourceKey:** The S3 object key for the SecurityHubEnabler Lambda deployment package.

- **ComplianceFrequency:** The frequency (in days) to check organizational compliance. The default is set to 7 days.

- **RoleToAssume:** The IAM role to be assumed in child accounts to enable Security Hub. The default is 'AWSControlTowerExecution' for a Control Tower environment.

- **AWSStandard:** Specify whether Security Hub should enable the AWS Foundational Security Best Practices v1.0.0 Security Standard.

- **CISStandard:** Specify whether Security Hub should enable the CIS Security Standard.

- **PCIStandard:** Specify whether Security Hub should enable the PCI DSS Security Standard.
