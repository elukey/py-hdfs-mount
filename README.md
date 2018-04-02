### Requirements

Python 3

### Install

```
pip install -r requirements.txt
```

### Running

```
kinit -kt $USER $USER@REALM

mkdir dest_mount
python hdfs_mount.py http://hdfs_hostname:50070 <hdfs-root-path> dest_mount <hdfs-user> <hdfs-group>
```

Have fun!

### Tested with


* [x] Vim (open file, edit randomly, save and close)

### Functionnalities


* [x] Cached writes (HDFS is an immutable FS (so writes=delete+insert))
* [x] Random writes (slow - because of the immutability of HDFS - but working!)
* [x] Very fast ls (cached directory metadata)
* [ ] directory stored as a zip file in HDFS (to solve small files problem)
* [ ] directory stored as a avro file in HDFS (to solve small files problem)
* [ ] CRC32 checksum
* [ ] Load options from configuration file


### Implemented FUSE methods

#### Basic
* [ ] access
* [x] chmod
* [ ] chown
* [x] getattr
* [x] readdir
* [ ] readlink
* [ ] mknod
* [x] rmdir
* [x] mkdir
* [ ] statfs
* [ ] unlink
* [ ] symlink
* [x] rename
* [ ] link
* [x] utimens

#### File methods

* [x] open
* [x] create
* [x] read
* [x] write
* [x] truncate
* [x] flush
* [x] fsync
* [x] release

