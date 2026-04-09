# AI Cloud Threat Detection Platform

## Overview
This project demonstrates a real-time AWS cloud security monitoring pipeline integrated with Splunk. It captures AWS API activity through CloudTrail, stores logs in S3, triggers notifications through SNS and SQS, and ingests those events into Splunk for detection and analysis.

The long-term goal is to extend this platform with an AI assistant capable of analyzing cloud security events, explaining suspicious activity, and supporting threat triage.

## Current Architecture
AWS CloudTrail → S3 → SNS → SQS → Splunk

## What I Built
- Enabled AWS CloudTrail to capture management event activity
- Configured S3 as centralized CloudTrail log storage
- Created SNS topic for event-driven log notifications
- Created SQS queue and dead-letter queue for reliable message delivery
- Configured IAM permissions for Splunk ingestion
- Integrated the pipeline with Splunk using the Splunk Add-on for AWS
- Verified live ingestion of CloudTrail events into Splunk

## Current Capabilities
- Searchable AWS CloudTrail logs in Splunk
- Visibility into IAM activity and AWS API calls
- Detection foundation for suspicious behavior such as:
  - failed API calls
  - IAM changes
  - reconnaissance activity
  - privilege escalation attempts

## Example Splunk Query
```spl
index=* sourcetype=aws:cloudtrail
