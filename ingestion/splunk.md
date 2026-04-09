# Splunk Integration

- Installed Splunk Enterprise
- Installed Splunk Add-on for AWS
- Configured SQS-based S3 input
- Connected to AWS account using access keys

## Result

CloudTrail logs are ingested in near real-time and indexed in Splunk.

## Example Query

index=* sourcetype=aws:cloudtrail
