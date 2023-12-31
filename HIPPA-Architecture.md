The **Quick** Start sets up the following:
A highly available architecture that spans two Availability Zones.
Three virtual private clouds (VPCs): management, production, and development. The VPCs are configured with subnets, according to AWS best practices, to provide you with your own virtual network on AWS.

In the **management VPC**:
The internet gateway serves as a highly available centralized point of egress for internet traffic.
Public subnets include managed network address translation (NAT) gateways to allow outbound internet access for resources in the private subnets.
Private subnets for deploying your security and infrastructure controls.
Flow logs for auditing

In the **production VPC**:
  Private subnets for deploying your production workloads.
  Flow logs for auditing.

In the **development VPC**:
  	Private subnets for deploying your development workloads.
  	Flow logs for auditing

AWS **Transit Gateway** for VPC-to-VPC communication and customer connectivity.

For **logging and audit controls**:
Amazon CloudWatch for metric monitoring and threshold alarms. This service delivers flow logs to an S3 bucket.
AWS Config with the conformance pack for HIPAA, maps HIPAA requirements to AWS configuration items. This service delivers flow logs to an S3 bucket.
AWS CloudTrail for AWS access logging. This service delivers flow logs to an S3 bucket.

For **access control and alerting:**
Amazon Simple Notification Service (Amazon SNS) for sending email alerts from alarms.
AWS Identity and Access Management (IAM) for access control and authorization
