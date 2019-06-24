# Services | Storage Gateway

## General

* connects on-premise to AWS infrastructure

## Types

* File Gateway (NFS)

    * files are stored as objects in your S3 buckets

    * accessed through a Network File System mount point

    * S3 features apply

    ![File Gateway](https://docs.aws.amazon.com/storagegateway/latest/userguide/images/file-gateway-concepts-diagram.png)

* Volume Gateway (iSCSI)

    * presents your applications with disk volumes using the iSCSI block protocol

    * data written to these vlumes can be asycnrhonously backed up as point-in-time snapshots of your volumes, and stored in the cloud as Amazon EBS snapshots

    * snapshots are incremental backups that capture only changed blocks. All snapwhot storage is also compressed to minimize your storage charges

    * Types:

        * Stored volumes

            * let you store your primiary data locally while asynchronously backing up that data to AWS

            * provide your on-premise applications with low-latency access to their entire dataset while providing durable, off-site backups

            * can be mounted as iSCSI deviecs from your on-promise application servers

            * stored on your on-premise storage hardware which is asynchronously backed up to Amazon S3 in form of Amazon EBS snapshots

            * 1 Gigabyte to 16 Terabyte in size

            ![Volume Gateway - Stored](https://docs.aws.amazon.com/storagegateway/latest/userguide/images/aws-storage-gateway-stored-diagram.png)

        * Cached Volumes

            * let you use Amazon S3 as your primary data storage while retaining frequently accessed data locally in your storage gateway

            * minimizes the need to scale your on-premise storaeg infrastructure while still providing your applications with low-latency access to their frequently accessed data

            * attached as iSCSI devices from your on-premises application servers

            * stored data that you write to these volumes in Amazon S3 and retains recently read data in your on-premises storage gateway's cache and upload buffer storage

            * 1 Gigabyte to 32 Terabytes in size

            ![Volume Gateway - Cached](https://docs.aws.amazon.com/storagegateway/latest/userguide/images/aws-storage-gateway-cached-diagram.png)

* Tape Gateway (Virtual Tape Library or VTL)

    * lets you leverage your existing tape-based backup application infrastructure to store data in virtual tape cartidges that you create on your tape gateway

    * each tape gateway is preconfigured with a media changer and tape drives which are available to your existing client backup applications as iSCSI devices

    * You add tape cartridges as you need to archive your data

    * Supported by NetBackup, Backup Exec, Veeam

    ![Tape Gateway](https://docs.aws.amazon.com/storagegateway/latest/userguide/images/Gateway-VTL-iSCSI-vtl-diagram.png)
