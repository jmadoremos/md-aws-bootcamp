# Exam Notes | Simple Storage Service (S3)

## General

* S3 is an object-based

* each file can be from 0 byte to 5 TB

* no limit to number of files

* files are stored in buckets (i.e., folder in the cloud)

* max of 100 S3 Buckets can be created. Limit can be increased by contacting the AWS Support

* S3 can now accommodate 3,500 PUTs per second

* S3 is a universal namespace. that is, names must be unique globally.

* sample valid URL: 

    * (path style): https://s3-us-east-1.amazonaws.com/acloudguru

    * (virtual-hosted style): https://acloudguru.s3.amazonaws.com

* not suitable to install an operating system

* successful upload will generate an **HTTP 200** status code

* you can turn on **MFA Delete**

* Key Fundamentals of S3

    * Key (name)

    * Value (data)

    * Version ID

    * Metadata (tagging)

    * Subresource

        * access control list

        * torrent

* Consistency Models

    * Read after Write consistency for PUTS of new objects (uploaded files can be read immediately)

    * Eventual Consistency for overwrite PUTS and DELETES (can take some time to propagate changes)

* Tiers / classes

    * S3 standard - 99.99% availability, 11x9s durability

    * S3 IA - infrequently accessed, requires rapid access, charged of retrieval fee

    * S3 One Zone IA - cheaper than IA but only stored in one availability zone with 99.50% availability

    * S3 Intelligent Tiering - optimize cost by automatically moving data to the most cost-effective access tier

    * S3 Glacier - archived data, average 3 to 5 hours

    * S3 Glacier Deep Archive - lowes-cost where retrieval time of 12 hours is acceptable

* Read S3 FAQs before taking the exam

* S3 is always Global region. But the buckets are region-specific.

* Allows client-side and server-side (eg., S3 Managed Keys, KMS, Customer Provided Keys) encryption

* by default, buckets are private and all objects stored inside are private

## Version Control

* stores all versions of an object (including all writes, and even if you delete an object)

* great backup tool

* once enabled, versioning cannot be disabled, only suspended

* integrates with lifecycle rules

* versioning's MFA Dete capability as additional layer of security
