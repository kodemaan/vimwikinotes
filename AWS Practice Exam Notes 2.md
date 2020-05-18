# Practice exam 2 notes
You can use DynamoDB for web sessions and storing metadata for Amazon S3 objects

You can use on premises and aws hosted resources for an application by utilizing
* SQS to use a queue to poll from both locations
* SWF to use a workflow to utilize both places, this is more for manual workflow vs queue

Glacier is used for Storing data archives, and storing infrequently accessed data.
Data ware house is wrong because redshift is best for data warehousing

Cloudwatch and SNS go together, SES does not

Global accelerator is more for non-HTTP traffic globally vs cloudfront that's better for http content
During RDS fail-over the canonical name record (CNAME) is switched from primary to standby instance to avoid downtime

The terminology for attaching ENI interfaces:
* Hot attach (while running)
* Warm attach (while stopped)
* Cold attach (when it's being launched for the first time)

Amazon DLM (Data Lifecycle Manager) manages EBS snapshot creation

AWS is responsible for the Physical network infrastructure for you, User access to the AWS environment is also your responsibility (eg. groups, users, etc.)

Canary deployments allow specifying the percentage of traffic shifted to your updated lambda function version before the remaining traffic is shifted in the second increment

Left off on Question 20 of the practice exam review
