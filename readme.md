# AWS Cloud Cost Optimization - Identifying Stale Resources

## Identifying Stale EBS Snapshots

In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

### Description:

The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.

## Overview  
This project implements an automated pipeline to identify and clean up stale AWS resources, such as unused EC2 instances, EBS volumes, and obsolete snapshots, significantly reducing cloud costs.  

## Features  
- **Automated Cleanup**: Identifies and deletes stale EC2 instances, unused EBS volumes, and obsolete snapshots using AWS Lambda and Boto3.  
- **Proactive Monitoring**: Configures CloudWatch alarms to monitor resource utilization and trigger real-time alerts for underutilized resources.  
- **Enhanced Security**: Implements robust IAM policies to enable least privilege access and ensure secure automation.  
- **EBS Optimization**: Deletes obsolete EBS snapshots while retaining necessary backups, reducing storage costs without compromising data integrity.  

## Tools and Technologies  
- **AWS Lambda**  
- **Amazon EC2**  
- **Amazon EBS**  
- **AWS IAM**  
- **Boto3**  
- **Amazon CloudWatch**  

## How It Works  
1. **Resource Discovery**:  
   - Fetches all EC2 instances and EBS volumes in the AWS account.  
   - Identifies unused or stale resources based on activity status and lifecycle policies.  

2. **Cleanup Automation**:  
   - Deletes unused EBS volumes and obsolete snapshots no longer associated with active resources.  
   - Removes stale EC2 instances based on predefined criteria.  

3. **Monitoring and Alerts**:  
   - CloudWatch alarms are configured to monitor resource utilization and alert on underutilization or anomalies.  

4. **Security**:  
   - IAM policies enforce least privilege access, ensuring secure execution of automation tasks.  

## Results  
- Achieved a **20% reduction** in monthly AWS cloud costs.  
- Improved resource utilization and enhanced security compliance across the cloud environment.  

## Getting Started  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/aws-cost-optimization.git


