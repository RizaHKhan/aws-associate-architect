# EC2

## Introduction

## Connecting

## Storage

- Direct (local) attached Storage - Storage on the EC2 Host
  -- Usually very fast
- Network attached storage - Volumes delivered over the network (EBS)
- Ephemeral Storage - Temporary Storage
- Persistent Storage - Permanent storage - lives on past the lifetime of the instance

Types of storage

- Block storage - Volume presented to the OS as a collection of blocks... no structure provided. Mountable. Bootable.
- File storage - Presented as a file share... has structure. Mountable. NOT Bootable.
- Object storage - collection of objects, flat. Not mountable. Not bootable.

## Storage Performance

Lots of factors determine storage performance

## Elastic Block Store (EBS)

**Availability Zone Based**

- Block storage - raw disk allocations (volume) - Can be encrypted using KMS
- ...instances see block device and create file system on this device (ext3/4, xfs)
- Storage is provisioned in **ONE AZ** (Resilient in that AZ)
- ...detached and reattached, not lifecycle linked to one instance... persistent
- Snapshot (backup) into S3. Create volume from snapshot (migrate between AZs)
- Different physical storage types, different sizes, different performance profiles
- Billed based on GB-month (and in some cases performance)

### Volume Types

- General Purpose SSD
- GP3 is better(?)

- Provisioned IOPS SSD (io1/2)

- HDD-based
  -- st1 Throughput Optimized
  --- cheap
  -- sc1 Cold HHD
  --- cheaper

- Instance Store Volumes
  -- Block storage devices
  -- Physically connected to one EC2 Host
  -- Instances on that host can access them
  -- Highest storage performance in AWS
  -- Included in instance price...
  -- **Attached at launch**

## EC2 Purchase Options (Launch Types)

### On-demand

The most basic

### Spot

SPOT pricing is AWS selling unused EC2 host capacity for up to 90% discount - the spot price is based on the spare capacity at a given time.

ON-DEMAND

**Never use SPOT for workloads which can't tolerate interruptions**

### Reserved

- No Reservation
  -- Full per\s price

- Matching instance, reduced or no p/s price
- Unused Reservation still billed
- Partial coverage of larger instance

### Dedicated Hosts

Allocated to the user in its entirety. That come will all the resources of a PC. User pays for the host. There is per/s charge. No instance charges.

### Dedicated Instance

User doesn't own, or share the host. Extra charges for instances, but dedicated hardware.
