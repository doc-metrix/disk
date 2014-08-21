Disk
===

A specification for disk performance metrics.


## Disk Types

- 	dm-{disk_number}: Logical drives mapped by the linux kernel's logical volume manager (LVM).
- 	loop{disk_number}: Loop devices used to mount filesystems not associated with block devices.
- 	md{disk_number}: Metadisk (RAID) devices. The metadisk driver is used to span a filesystem across multiple physical disks.
- 	ram{disk_number}: RAM disks. A maximum of 250 RAM disk are allowed.
- 	sd{disk_letter}: Small computer system interface (SCSI) disk devices. Disk letters range from a to p, allowing for a maximum of 16 devices. Each device can have a maximum of 15 partitions.
- 	sd{disk_letter}{partition_number}: Partitions on the SCSI device. Each device can have a maximum of 15 partitions.


## Contributing

To contribute to this specification, see the contributing [guide](https://github.com/doc-metrix/contributing). Any updates to the specification should be tagged.

``` bash
$ git tag -a <major.minor.patch> -m "[UPDATE] version."
$ git push origin <major.minor.patch>
```

Use [semantic versioning](http://semver.org/) (semvar) for communicating versions. For example, any new metrics should be communicated as `minor` updates, while any corrections should be `patches`. Any specification restructuring (changing field names, removing fields, etc) should be communicated as `major` updates.


## Usage

The specification is stored as [JSON](http://json.org/), a lightweight data-interchange format. Many languages provide JSON support: [JavaScript](http://www.json.org/js.html), [Python](https://docs.python.org/2/library/json.html), [Go](http://golang.org/pkg/encoding/json/), [PHP](http://php.net/manual/en/book.json.php), [Java](http://json.org/java/), [Haskell](http://hackage.haskell.org/package/json), and [others](http://json.org/).

You are free to use the JSON specification, as is. Simply copy the file and use accordingly.

For those using package managers to manage dependencies, we provide package manager support, as outlined below.


### Bower

The specification is registered as a [Bower](http://bower.io) package. Bower provides a straightforward means for managing dependencies.

In order to use Bower, you must first install [Node.js](http://nodejs.org/) and [Git](http://git-scm.com/book/en/Getting-Started-Installing-Git). Once the prerequisites are installed,

``` bash
$ npm install -g bower
```

To [install](http://bower.io/docs/api/#install) the latest specification,

``` bash
$ bower install doc-metrix-disk
```

Bower will place the specification in a `bower_components/` directory within the current working directory.

To [update](http://bower.io/docs/api/#update) to the latest specification,

``` bash
$ bower update doc-metrix-disk
```


### Utilities


---
## License

[MIT license](http://opensource.org/licenses/MIT). 


---
## Copyright

Copyright &copy; 2014. NodePrime.

