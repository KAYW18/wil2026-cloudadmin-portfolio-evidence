# Week 3 – Ops Automation Lite

## Project Name
S3 Vault Health Check using AWS Lambda

## 1. Purpose
The purpose of this automation is to reduce repeated manual checking of my S3 bucket security settings. The Lambda function will check whether the bucket's main security settings are correctly configured and report the results.

## 2. Problem Being Solved
Checking Block Public Access, encryption and versioning manually takes time. Automating these checks makes it easier to review the bucket settings consistently.

## 3. Automation Design
- Track: B – AWS Lambda
- Function name: wil-week3-s3-vault-health-check
- Trigger: Manual test from the Lambda console
- Action: Check S3 security settings and log the results.
- Output: PASS or FAIL results in CloudWatch Logs.

## 4. Security Checks
- Block Public Access: All four settings must be enabled.
- Encryption: SSE-S3 must be configured.
- Versioning: Must be enabled.

## 5. Permissions
The Lambda execution role will use only the permissions required to read the S3 bucket configuration and write logs to CloudWatch.

## How to run
1. Open the Lambda function in AWS.
2. Select the saved test event.
3. Click Test.
4. Review the output and CloudWatch logs.

## 7. Expected Result
The Lambda function runs successfully and checks the selected S3 bucket's Block Public Access settings, SSE-S3 encryption and versioning. The results are displayed in CloudWatch Logs.

## 8. Risk Reduced
This automation reduces the risk of overlooking important S3 security settings during manual reviews.

## 9. Evidence
- Lambda function successfully created.
- Python automation code deployed.
- Successful manual test execution.
- CloudWatch Logs showing the security check results.
- IAM role and read-only S3 permissions.
- Resource tags applied.

## Limitations
- Checks only the configured bucket.
- Checks only when invoked.
- Does not change settings.
- Does not inspect individual objects.
