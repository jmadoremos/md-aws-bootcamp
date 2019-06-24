# Exam Notes | Elastic Compute 

* On demand - allows to pay fixed rate by the hour or second with no commitment

* Reserved - provides you with a capacity reservation and offer significant discount on the hourly charge

* Spot - enabled you to bid whatever price you want for the instance capacity

* Dedicated Hosts - physical EC2 server dedicated for your use

* If a spot instance is terminated by AWS EC2, you will not be charged for a partial hour of usage

* If you terminate the instance yourself, you will be charged for the complete hour in which the instance ran

* FIGHT DR MC PX

* SSD: General Purpose - balances price and performance

* SSD: Provisioned IOPS - highest-performance SSD

* Magnetic: Throughput Optimized HHD - low cost HHD for frequently accessed, throughput-intensive workloads

* Magnetic: Cold HHD - lowest cost HHD for less frequently accessed workloads

* Magnetic: Standard - Previous generation but can be used as boot volume

* Termination Protection is turned off by default, you must turn it on

* On an EBS-backed instance,t he default action is for the root EBS volume to be deleted when the instance is terminated

* EBS Root Volumes of your DEFAULT AMI's cannot be encrypted. You can also use a third party tool (such as bitlocker, etc.) to encrypt the root volume, or this can be done when creating AMI's in the AWS console or using API

* Additional volumes can be encrypted
