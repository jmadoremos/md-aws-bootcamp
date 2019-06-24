# Services | Simple Storage Service (S3)

## Definition and Features

* object-based - allows you to upload files

* each file can be from 0 byte to 5 TB

* unlimited number of files to 

* Files are stored in buckets (ie., folder with universal name/URL stored in the cloud)

* bucket names are unique 

* bucket names must be DNS compliant (no uppercase and underscore, 3 <= len(bucket name) < 63):

    * (old url): https://s3-{region name}.amazonaws.com/{bucket name}/

    * (virtually-hosted-style, new url): https://{bucket name}.s3.amazonaws.com

* HTTP 200 - upload is successful

* 99.99% availability, amazon guaranteed

* 99.9999999999% (11 9's) durability

* features:

    * tiered storage available

    * lifecycle management

    * versioning

    * encryption

    * MFA delete

    * secure data using access control list (i.e., individual file) or bucket policies (i.e., entire file)

## Data Consistency Model

* read after write consistency for PUTS of new Objects

    * can be read immediately

    * applicable for newly created objects

* eventual consistency for overwrite PUTS and DELETES (can take some time to propagate)

    * if a file is renamed then immediately read, there may be two results produced (1) the original file with its original filename, and (2) the renamed file with new filename

    * applicable for updates on existing objects

## Key Value Store

* key - name of the object

* value - data made up of bytes

* version id - versioning

* metadata - tagging

* subresources

    * access control list

    * torrent

## Storage Tiers and Classes

* S3 Standard

    * 99.99% availability

    * 11 9's% dirability

    * stored redundantly across multiple devices in multiple facilities

    * guaranteed to sustain loss of 2 facilities concurrently

* S3 Standards IA

    * infrequently accessed

    * for data that is access less frequently but requires rapid 

    * charged a retrieval fee

* S3 One Zone IA

    * S3 IA stored in one zone

    * 99.50% availability

* S3 Intelligent Tiering

    * Optimize costs by automatically moving data to the most cost-effective access tier without performance impact or operational overhead

* Glacier

    * low-cost storage for data archiving

    * expedited - restored within a few minutes, require higher fee

    * standard - 3 to 5 hours

    * bulk - 5 to 12 hours

* Glacier Deep Archive

    * lowest-cost storage class where a retrieval time of 12 hours is acceptable

## Charging

* storage

* requests

* storage management pricing (eg, tiers)

* data transfer pricing (e.g., retrieval)

* transfer acceleration

* cross-region replication (e.g., moving data across region)

## Cross Region Replication

* replicate an object to another bucket in another region for high availability and disaster recovery

* Versioning must be enabled on both source and destination buckets

* Regions must be unique

* Files in an existing bucket are not replicated automatically. All subsequent updated files are replicated automatically.

* You cannot replicate to multiple buckets or use daisy chaining

* When a file is deleted in the source, a delete marker is placed on that version in the source. however, the same file replicated in the destination remains the same (without delete marker and still visible in the view).

* Deleting individual versions or delete markers will not be replicated

## Transfer Acceleration

* fast, easy and secure transfer of files

* uses CloudFront edge locations (ie., the user uploads a file, AWS takes the file to the nearest edge location to upload. once uploaded, AWS will move the file to the S3 bucket)

## Encryption

* by default, all newly created buckets are **private**

* access control using:

    * bucket policy

    * access control list

* Encryption in transit - data is on the move

    * achieved by SSL and TLS

* Encryption at rest - data is on a storage

    * server side - data is encrypted in S3

        * **S3 Managed Keys (SSE-S3)** where amazon manages all the keys

        * **AWS Key Management Service (SSE-KMS)** where amazon and customer manages the keys together

        * **Server-size Encryption with Customer Provided Keys (SSE-C)**

    * client side - data is encrypted before storing to S3

## Version Control

* stores all versions of an object (including all writes and even if you delete an object)

* great for backups

* Once enabled, **versioning cannot be disabled** but can be suspended

* integrates with **Lifecycle rules**

* Avoid versioning if the file is very large and frequently changed since this will create multiple copies of the file which will increase the storage size significantly

* To restore an old version, either overwrite the latest with the old version or delete the latest version then delete the delete marker which is hidden

* you can enable bucket for **MFA Delete** which will require MFA when an object is about to be deleted

## Lifecycle Management

* can be used in conjuction with versioning

* can be applied to current versions and previous 

* following actions can now be done:

    * transition to S3 IA (defaults to 30 days after creation date)

    * archive to Glacier (default to 30 days after IA)

    * permanently delete
