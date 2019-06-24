# Services | Elastic Compute Cloud

## General

* virtual machine in the cloud

* web service that provides resizable compute capacity in the cloud

* reduces the time required to obtain and boot new server instances to minutes, allowing quick scale capacity

## EC2 Options

* On Demand - paid by the second or hour depending on the instance type

* Reserved Instances

    * Contract terms are 1 year to 3 years

    * Types:

        * Standard RI - 1 to 3 years commitment (up to 75% off compared to on-demand)

        * Convertible RI - RI where the instance type may be changed to another of equal or greater value

        * Scheduled RI - timed window of reservation (eg., fraction of a day, a week, or a month)
    
* Spot Instances - flexible start and end times; urgent need for large compute capacity

* Dedicated Host - not multi-tenant; can bring your own license; can be purchased on demand (hourly) or reserved (up to 70% off compared to on-demand)

## EC2 Instance Types

* F1 - field programmable gate array (eg., genomics research, financial analytics)

* I3 - high speed storage (eg., NoSQL, Data Warehousing)

* G3 - graphics intensive (eg., Video Encoding)

* H1 - high disk throughput (eg., MapReduce)

* T2 - lowest cost, general purpose (eg., small web servers/db)

* D2 - dense storage (eg., fileservers/hadoop)

* R4 - memory optimized (eg., memory extensive apps/db)

* M5 - general purposed (eg., app servers)

* C5 - compute optimized (eg., cpu intensive apps/db)

* P3 - graphics/general purpose GPU (eg., machine learning, bitcoin mining)

* X1 - memory optimized (eg., sap hana, apache spark)

## Elastic Block Storage (EBS)

* for OS, Applications, etc

* does not existing on one disk only, but replicated to other disks for redundancy

## EBS Volume Types

* Flash: General Purpose SSD (GP2)

    * 3 IOPS per GB with up to 10,000 IOPS

    * burst up to 3,000 IOPS for extended periods

* Flash: Provisioned IOPS SSD (IO1)

    * designed for I/O intensive application
    
    * more than 10,000 IOPS

    * can provision upto 20,000 IOPS per volume

* Magnetic: Throughput Optimized HDD (ST1)

    * cannot be boot volume, but as an additional volume

    * used for big data, data warehouses, log processing

* Magnetic: Cold HDD (SC1)

    * cannot be boot volume, but as an additional volume

    * lowest cost storage for infrequent accessed workloads

    * for file servers

* Magnetic: Standard

    * can be used as boot volume

    * lowest cost per GB of all bootable volume types

## Launching EC2 Instances

* 1 subnet is assigned to 1 specific availability zone only

* Under Advanced Details section, for the User Data field, you can enter bootstrap scripts to EC2 instance to perform specific actions (e.g. download apache, start apache) which is ran every start of the instance

* What happens to EBS instance when the EC2 is deleted? By default EBS is also deleted. This is configured under "Delete on Termination" column of "Add Storage" step when creating a new instance

* When Security Group's Source column has an "anywhere" or "0.0.0.0/0" value, there is always a warning stating that the security group is accessible to the internet

* Tags are sorted alphabetically

* "chmod 400 *.pem" to prevent accidental overwriting of the private key files

* A "Default VPC" is auto-created when creating an AWS account. Accompanying that VPC is an auto-created Security Group

* System Status Check is checking the  underlying AWS Hypervisor

* Instance Status Check is checking the traffic of the operating system

* You can encrypt other volumes but by default, you cannot encrypt the boot volume of AWS images
