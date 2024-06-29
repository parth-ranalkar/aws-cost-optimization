# AWS Cloud Cost Optimization - Identifying Stale Resources

## Identifying Stale EBS Snapshots

In this project, I've developed a Lambda function that proactively identifies and deletes EBS snapshots no longer associated with any active EC2 instances. This automated process helps save on storage costs by ensuring that unused snapshots are efficiently cleaned up.

### Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

### Screenshots:

- Created EC2 Instance on AWS
  
  ![1](https://github.com/parth-ranalkar/aws-cost-optimization/assets/73604763/af555402-12ac-4ae4-8420-1069c3755ed2) 

> [!NOTE]
> _Already there was one EC2 instance I created earlier , That's why it's showing 2 instances._

  ![2](https://github.com/parth-ranalkar/aws-cost-optimization/assets/73604763/817fcb09-27a3-473c-815c-f7556f0ea7e9)

- Took snapshot of EC2
  
  ![3](https://github.com/parth-ranalkar/aws-cost-optimization/assets/73604763/0d388f9a-ebbd-49a4-b7ca-b27ed0513932)
  
- Terminated EC2
  
  ![4](https://github.com/parth-ranalkar/aws-cost-optimization/assets/73604763/df54934d-c54d-47b6-a2f4-81510c73d1e3)
  
- Stale Snapshot Count
> [!NOTE]
> _After terminating EC2 the snapshot is still there on AWS._

  ![5](https://github.com/parth-ranalkar/aws-cost-optimization/assets/73604763/3996a855-e4dc-4071-a923-124d7112fbbf)

- After Running AWS Lambda Function
  
![6](https://github.com/parth-ranalkar/aws-cost-optimization/assets/73604763/f168e0a3-726f-44fd-8ed2-2f70715d0773)


