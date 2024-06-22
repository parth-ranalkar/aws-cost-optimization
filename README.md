# AWS Cloud Cost Optimization - Identifying Stale Resources

## Identifying Stale EBS Snapshots

In this project, I've developed a Lambda function that proactively identifies and deletes EBS snapshots no longer associated with any active EC2 instances. This automated process helps save on storage costs by ensuring that unused snapshots are efficiently cleaned up.

### Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.



