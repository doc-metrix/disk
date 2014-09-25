Disk
===

> Documentation for disk performance metrics.


## Metrics

#### [disk.ioInProgress](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of I/O operations currently in progress. The metric is incremented as requests are submitted and decremented as requests finish. The metric does not include requests that are in queue waiting to be submitted.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | [I/O](https://github.com/doc-metrix/units#io) | raw | [integer](https://github.com/doc-metrix/data-types#integer)


#### [disk.readsIssued](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of reads completed successfully.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | reads | raw | [count](https://github.com/doc-metrix/data-types#count)


#### [disk.readsMerged](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of adjacent reads merged for read efficiency. For example, two 4K reads may become one 8K read before being ultimately handed to the disk. The merged read will be queued (and counted) as only one I/O.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | reads | raw | [count](https://github.com/doc-metrix/data-types#count)


#### [disk.sectorsRead](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of sectors read successfully.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | sectors | raw | [count](https://github.com/doc-metrix/data-types#count)



#### [disk.sectorsWritten](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of sectors written successfully.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | sectors | raw | [count](https://github.com/doc-metrix/data-types#count)



#### [disk.timeDoingIO](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of milliseconds spent processing IO requests. This metric only increases when the number of I/Os in progress is nonzero.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | [ms](https://github.com/doc-metrix/units#ms) | raw | [time](https://github.com/doc-metrix/data-types#time)


#### [disk.timeReading](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of milliseconds spent by all reads. 

Note: A possibility exists that this value will overflow and wrap on a 32-bit system that has been continuously running for an extended time.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | [ms](https://github.com/doc-metrix/units#ms) | raw | [time](https://github.com/doc-metrix/data-types#time)


#### [disk.timeWriting](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of milliseconds spent by all writes. 

Note: A possibility exists that this value will overflow and wrap on a 32-bit system that has been continuously running for an extended time.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | [ms](https://github.com/doc-metrix/units#ms) | raw | [time](https://github.com/doc-metrix/data-types#time)



#### [disk.writesCompleted](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of writes completed successfully.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | writes | raw | [count](https://github.com/doc-metrix/data-types#count)



#### [disk.writesMerged](https://www.kernel.org/doc/Documentation/iostats.txt)

The number of adjacent writes merged for write efficiency. For example, two 4K writes may become one 8K write before being ultimately handed to the disk. The merged write will be queued (and counted) as only one I/O.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | writes | raw | [count](https://github.com/doc-metrix/data-types#count)



#### [disk.weightedTimeDoingIO](https://www.kernel.org/doc/Documentation/iostats.txt)

The weighted amount of time processing I/Os that is incremented every time the number of I/Os in progress is updated. The stepwise increment is equal to the number of I/Os in progress multiplied by the number of milliseconds spent doing I/Os since the last time number of I/Os in progress was updated. This can provide an easy measure of both I/O completion time and the backlog that may be accumulating.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `MAX_UNSIGNED_LONG` | [ms](https://github.com/doc-metrix/units#ms) | raw | [time](https://github.com/doc-metrix/data-types#time)



#### [disk.size](http://linux.die.net/man/1/df)

The total size of the file system.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `null` | [GB](https://github.com/doc-metrix/units#GB) | raw | [numeric](https://github.com/doc-metrix/data-types#numeric)


#### [disk.used](http://linux.die.net/man/1/df)

The amount of disk space allocated to existing files in the file system.

Note: The maximum value is the total size of the file system.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `null` | [GB](https://github.com/doc-metrix/units#GB) | raw | [numeric](https://github.com/doc-metrix/data-types#numeric)



#### [disk.available](http://linux.die.net/man/1/df)

The amount of space available within the file system for the creation of new files by unprivileged users. When this value is less than or equal to zero, it will not be possible to create any new files on the file system without first deleting others, unless the process has appropriate privileges.

Note: The maximum value is the total size of the file system. The minimum value can be less than 0.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
`null` | `null` | [GB](https://github.com/doc-metrix/units#GB) | raw | [numeric](https://github.com/doc-metrix/data-types#numeric)



#### [disk.spaceUtilization](http://linux.die.net/man/1/df)

The disk space utilization (used storage divided by total size) for an individual disk.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | 1 | [utilization](https://github.com/doc-metrix/units#utilization) | derived | [percentage](https://github.com/doc-metrix/data-types#percentage)


#### [disk.spaceUtilizationAverage](http://linux.die.net/man/1/df)

The average disk space utilization (used storage divided by total size) across all disks.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | 1 | [utilization](https://github.com/doc-metrix/units#utilization) | derived | [percentage](https://github.com/doc-metrix/data-types#percentage)



#### [disk.timeUtilization](http://linux.die.net/man/1/df)

The disk time utilization (time spent doing I/O operations in a measurement interval divided by that interval) for an individual disk.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | 1 | [utilization](https://github.com/doc-metrix/units#utilization) | derived | [percentage](https://github.com/doc-metrix/data-types#percentage)



#### [disk.timeUtilizationAverage](http://linux.die.net/man/1/df)

The average disk time utilization (time spent doing I/O operations in a measurement interval divided by that interval) across all disks.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | 1 | [utilization](https://github.com/doc-metrix/units#utilization) | derived | [percentage](https://github.com/doc-metrix/data-types#percentage)


#### [disk.readRate](http://linux.die.net/man/1/df)

The amount of data read divided by the time spent reading on an individual disk since the last reboot.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `null` | [MB/s](https://github.com/doc-metrix/units#mbs) | derived | [numeric](https://github.com/doc-metrix/data-types#numeric)



#### [disk.readRateAverage](http://linux.die.net/man/1/df)

The average of data read divided by time spent reading across all disks since the last reboot.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `null` | [MB/s](https://github.com/doc-metrix/units#mbs) | derived | [numeric](https://github.com/doc-metrix/data-types#numeric)



#### [disk.writeRate](http://linux.die.net/man/1/df)

The amount of data written divided by the time spent writing on an individual disk since the last reboot.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `null` | [MB/s](https://github.com/doc-metrix/units#mbs) | derived | [numeric](https://github.com/doc-metrix/data-types#numeric)



#### [disk.writeRateAverage](http://linux.die.net/man/1/df)

The average of data written divided by time spent writing across all disks since the last reboot.

Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `null` | [MB/s](https://github.com/doc-metrix/units#mbs) | derived | [numeric](https://github.com/doc-metrix/data-types#numeric)



#### [disk.readWriteRatio](http://linux.die.net/man/1/df)

The ratio of data read divided by data written on an individual disk since the last reboot.


Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `inf` | `null` | derived | [numeric](https://github.com/doc-metrix/data-types#numeric)



#### [disk.readWriteRatioAverage](http://linux.die.net/man/1/df)

The average ratio of data read divided by data written across all disks since the last reboot.


Min | Max | Units | Metric Type | Data Type 
:---: | :---: | :---: | ---: | ---: |
0 | `inf` | `null` | derived | [numeric](https://github.com/doc-metrix/data-types#numeric)


## Notes

#### Disk Types

- 	`dm-<disk_number>`
	* 	Logical drives mapped by the Linux kernel's logical volume manager (LVM).
- 	`loop<disk_number>`
	* 	Loop devices used to mount filesystems not associated with block devices.
- 	`md<disk_number>`
	* 	Metadisk (RAID) devices. The metadisk driver is used to span a filesystem across multiple physical disks.
- 	`ram<disk_number>`
	* 	RAM disks.
	* 	The Linux kernel allows for a maximum of 250 RAM disks.
- 	`sd<disk_letter>`
	* 	Small computer system interface (SCSI) disk devices.
	* 	The Linux kernel allows disk letters ranging from `a` to `p` (a maximum of 16 devices), where each device can have a maximum of 15 partitions.
- 	`sd<disk_letter><partition_number>`
	* 	Partitions on the SCSI device.
	* 	The Linux kernel allows each device to have a maximum of 15 partitions.


## Contributing

To contribute to this documentation, see the contributing [guide](https://github.com/doc-metrix/contributing). Any updates to the documentation should be tagged.

``` bash
$ git tag -a <major.minor.patch> -m "[UPDATE] version."
$ git push origin <major.minor.patch>
```

Use [semantic versioning](http://semver.org/) (semvar) for communicating versions.

*	Any new metrics should be communicated as `minor` updates.
*	Any corrections/value modifications should be `patches`.
* 	Any documentation restructuring (changing field names, removing fields, etc) should be communicated as a `major` update.



## Usage

The documentation is stored as [JSON](http://json.org/), a lightweight data-interchange format. Many languages provide JSON support: [JavaScript](http://www.json.org/js.html), [Python](https://docs.python.org/2/library/json.html), [Go](http://golang.org/pkg/encoding/json/), [PHP](http://php.net/manual/en/book.json.php), [Java](http://json.org/java/), [Haskell](http://hackage.haskell.org/package/json), and [others](http://json.org/).

You are free to use the JSON documentation, as is. Simply copy the file and use accordingly.

For those using package managers to manage dependencies, we provide package manager support, as outlined below.


### Bower

The documentation is registered as a [Bower](http://bower.io) package. Bower provides a straightforward means for managing dependencies.

In order to use Bower, you must first install [Node.js](http://nodejs.org/) and [Git](http://git-scm.com/book/en/Getting-Started-Installing-Git). Once the prerequisites are installed,

``` bash
$ npm install -g bower
```

To [install](http://bower.io/docs/api/#install) the latest documentation,

``` bash
$ bower install doc-metrix-disk
```

Bower will place the documentation in a `bower_components/` directory within the current working directory.

To [update](http://bower.io/docs/api/#update) to the latest documentation,

``` bash
$ bower update doc-metrix-disk
```


### Utilities

List of utilities using this documentation:

*	[Node.js Module](https://github.com/doc-metrix/disk-node)


---
## License

[MIT license](http://opensource.org/licenses/MIT). 


---
## Copyright

Copyright &copy; 2014. [NodePrime](http://nodeprime.com).

