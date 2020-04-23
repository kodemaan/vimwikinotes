POSIX-compliance means EFS
S3 does not have folders so that doesn't work
SAML WAF uses external providers and not active directory

EC2 and EMR both utilize EC2 instances which you can access the underlying OS of, EMR provides managed Hadoop framework on top of an EC2 instance

Instance store means data will be deleted when volume is stopped

With Aurora you can create a reader endpoint that allows you to setup a reader endpoint which load-balances all queries across all aurora replicas.

Amazon Macie is ML-powered security service that helps you prevent data loss by automatically discovering, classifying, and protecting sensitive data stored in Amazon S3.

Guard duty protects against threats but does not do anything in regards to protecting PII data

In dynamoDB having more distinct values means more partitions and less chance of having a hot partition. If you have less distinct values that means that you have more of a chance to have hot partitions.

To make an application with stateless web servers you need a place to store the state. Two places you can do this are DynamoDB and ElastiCache. DynamoDB is object based DB that can store key - value pairs, and ElastiCache specializes in key-value storage

To make API Gateway more performant you can enable throttling limits and result caching. This will help limit calls to the backend for the api gateway calls and will make it faster if the request is already cached

In order to limit traffic into a whole VPC use a Network ACL, and to limit traffic to just an EC2 instance use a security group.

If on premise server already has message broker service using industry standard messaging apis use Amazon MQ because it's closes to that. Amazon SQS is fully managed but does not support all industry standard messaging APIs

To secure secrets use AWS Systems Manager Parameter Store or AWS Secrets manager. It's best practice to use an IAM role to secure this resource

When an elb health check fails an Auto Scaling group by default it does not disable or replace the instances. The auto scaling group has to be configured to do so

## CloudWatch default metrics:
* CPU
* Network
* Disk Performance
* Disk Reads/Writes

## Cloudwatch Advanced metrics (require script or other custom metric)
* Memory Utilization
* Disk Swap Utilization
* Page file utilization
* Log Collection

## TO LEARN
* Aurora
* Macie
* DynamoDB
* ECS
* Auto Scaling groups

Highly available means at least two availability zones

EBS snapshots are asynchronous which means that they can be done while the volume is in use

If ELB Health check fails it stops sending traffic to the EC2 host and that's it, it doesn't do anything else

When talking about flexible schema chances are you'll use a nosql database. This could also mean DynamoDB but doesn't necessarily always mean DynamoDB

S3 has server-side and client-side encryption for data in S3 to help secure confidential documents

Signed cookies allow access to many files whereas signed urls provide access to a single file. There are certain scnearios such as RTP where you need signed URL's but for the most part a signed cookie is fine.

If you want to view special metrics on RDS such as CPU consumed by each process on an RDS instance enable Enhanced Monitoring

You can authenticate and secure Redis via --transit-encryption-enabled and --auth-token parameters. 

Aurora serverless DB is a relational database that allows scaling up and down automatically. You can set minimum and maximum capacity for the cluster. 

Re-learn types of hard drives on AWS
* Small and random workloads are SSD and large sequential workloads are good for HDD

Cloudwatch Events allow reacting to a specific event and performing another event. This is easier than setting up a CloudWatch alarm

Can enable lambda environment variable encryption using a KMS key

If you want to give users access to an S3 bucket you can Setup a federation proxy or an identity provider and use AWS Security Token Service to generate temporary tokens, and then configure an IAM role and IAM policy to access the bucket

S3 client side encryption and client side master key if you have requirements that the encryption key cannot be shared with AWS

Kinesis firehose can load streaming data into elasticsearch

If you want to use an in memory cache two good solutions are Amazon ElastiCache or Redis but elasticache is a managed service

AMI's are only available in the region that they are made in. In order to share across regions you need to Copy it over to another region.

For Amazon Redshift Enhanced VPC Routing it forces all COPY and UNLOAD traffic to go through your VPC and allows using features such as security groups, ACL's, VPC endpoints, VPC endpoint policies, internet gateways, and DNS servers

Improve write throughput by Increasing EC2 instance size and using RAID 0 with two EBS Volumes, Raid 1 is for fault tolerance and not increasing performance

110.238.98.71/32 allows only a single IP address

## IAM DB Authentication
Allows authenticating with a database using ann authentication token. 
RDS gives permissions 

ROA (Route Origin Authorization) is a document that you can create through RIR (Regional Internet Registry) or RIPE (Reseaux IP Europeens Network Coordination Centre). This authorizes amazon to bring address range to AWS. You need to public a self signed X509 certificate in the RDAP remakrs for the address range which allows authorizing route to your aws account

To log events globally you need cloudtrail with is-multi-region-trail and include-global-service-events

When you reserve an instance you only can reserve it for a specific region per reservation

AWS RAM (Resource Access Manager) allows sharing resources between multiple AWS accounts

To continue - *Question 49*: [Practice Exam Results 1](https://www.udemy.com/course/aws-certified-solutions-architect-associate-amazon-practice-exams-saa-c02/learn/quiz/4394970/result/282096878#overview)
