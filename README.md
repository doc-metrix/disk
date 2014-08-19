Disk Metrics
===

Disk performance metrics.


## Disks Types In These Metrics

- dm-{disk_number}: Logical drives mapped by the linux kernel's logical volume manager (LVM).
- loop{disk_number}: Loop devices used to mount filesystems not associated with block devices.
- md{disk_number}: Metadisk (RAID) devices. The metadisk driver is used to span a filesystem across multiple physical disks.
- ram{disk_number}: RAM disks. A maximum of 250 RAM disk are allowed.
- sd{disk_letter}: Small computer system interface (SCSI) disk devices. Disk letters range from a to p, allowing for a maximum of 16 devices. Each device can have a maximum of 15 partitions.
- sd{disk_letter}{partition_number}: Partitions on the SCSI device. Each device can have a maximum of 15 partitions.


## License

[MIT license](http://opensource.org/licenses/MIT). 


---
## Copyright

Copyright &copy; 2014. NodePrime.

