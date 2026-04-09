# Architecture Overview

This project implements a real-time AWS security monitoring pipeline.

## Data Flow

1. AWS CloudTrail captures API activity
2. Logs are stored in S3
3. S3 triggers SNS notifications
4. SNS sends messages to SQS
5. Splunk polls SQS and retrieves logs
6. Events are indexed and searchable in Splunk

## Design Benefits

- Decoupled ingestion pipeline
- Real-time event-driven processing
- Scalable and production-relevant architecture
