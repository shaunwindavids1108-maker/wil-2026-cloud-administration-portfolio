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
The Lambda execution role has read-only permissions to check the selected S3 bucket settings. It also has permission to send execution logs to CloudWatch.

6. How to Run
Open the AWS Lambda console.

Select wil-week3-s3-vault-health-check.

Open the Code tab.

Select the Day2VaultHealthCheck test event.

Click Test to run the function.

Review the execution result to see the S3 security check results.

Open CloudWatch Logs to review the recorded report.

7. Expected Result
The function should check Block Public Access, default encryption and versioning. Each check should display PASS when the expected setting is correctly configured

8. Risk Reduced
This automation reduces the risk of overlooking important S3 security settings during manual reviews.

9. Evidence
Screenshots of the Lambda function, successful test execution and CloudWatch Logs will be added here.

## 10. Limitations
The function checks the bucket-level public access settings, default encryption configuration and versioning status. It does not automatically fix incorrect settings, inspect every uploaded object's encryption, or monitor the entire AWS account.

The function currently uses a manual test event and does not run automatically on a schedule.
