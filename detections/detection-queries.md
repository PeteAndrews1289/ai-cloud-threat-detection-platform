# Detection Queries

## Failed API Calls
index=* sourcetype=aws:cloudtrail errorCode=*

## IAM Privilege Changes
index=* sourcetype=aws:cloudtrail (AttachUserPolicy OR PutUserPolicy)

## Root Account Usage
index=* sourcetype=aws:cloudtrail userIdentity.type=Root

## Recon Activity
index=* sourcetype=aws:cloudtrail (List* OR Describe*)
