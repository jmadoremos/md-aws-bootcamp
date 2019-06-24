# Exam Notes | Storage Gateway

* connects on-premise to AWS infrastructure

* types:

    * File Gateway (NFS) - object-based. flatfiles in S3
    
    * Volume Gateways (iSCSI) - block-based. storage for OS, application
    
        * stored volumes - store entire copy on premise asynchronously backed up to S3. upto 16TB

        * cached volumes - store only most recent accessed data on premise, the rest are stored in cloud. upto 32TB

    * Taped Gateway (Virtual Tape Library or VTL) - file archiving and backup. NetBackup, Backup Exec, Veeam
