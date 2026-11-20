Week 3 – Ops Automation Lite

Project Name
S3 Vault Health Check using AWS Lambda

1. Purpose
The purpose of this automation is to reduce repeated manual checking of my S3 bucket security settings. The Lambda function will check whether the bucket's main security settings are correctly configured and report the results.

2. Problem Being Solved
Checking Block Public Access, encryption and versioning manually takes time. Automating these checks makes it easier to review the bucket settings consistently.

3. Automation Design
- Track:B – AWS Lambda
- Function name: wil-week3-s3-vault-health-check
- Trigger: Manual test from the Lambda console
- Action: Check S3 security settings and log the results.
- Output: PASS or FAIL results in CloudWatch Logs.

4. Security Checks
- Block Public Access: All four settings must be enabled.
- Encryption: SSE-S3 must be configured.
- Versioning: Must be enabled.

5. Permissions
The Lambda execution role will use only the permissions required to read the S3 bucket configuration and write logs to CloudWatch.

6. How to Run
To be completed after creating and testing the Lambda function.

7. Expected Result
The Lambda function should run successfully and report the status of the three S3 security checks.

8. Risk Reduced
This automation reduces the risk of overlooking important S3 security settings during manual reviews.

9. Evidence
Screenshots of the Lambda function, successful test execution and CloudWatch Logs will be added here.

## 10. Limitations
The function only checks the selected S3 bucket's configuration. It does not automatically fix incorrect settings or monitor the entire AWS account.
