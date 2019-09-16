# ZFS
@SmartOS, @Solaris, @FreeBSD

Compression
-----------
caveat - compression is *not* retroactive, so you should set it on the pool
immediately after creation



 # See compression settings
 zfs get compression
 # See compression efficiency
 zfs get compressratio
 # Set compression (types: lzjb, lz4, gzip-[1-9])
 zfs set compression=<type> <pool>

Delegate administrative tasks
-----------------------------
<https://blogs.oracle.com/marks/entry/zfs_delegated_administration>



 zfs allow

Snapshots
---------


  # List snapshots
  zfs list -t snapshot
  # Delete a snapshot
  zfs destroy tank/home/thing@tuesday

Rollback
--------

By default, ZFS rollback cannot revert to anything beyond the most recent snapshot. -r lets you go earlier, although this is a destructive operation and deletes the intermediate snapshots



  zfs rollback tanks/home/dave@tuesday

See disks
---------


  zpool list

References
----------


* <http://www.solarisinternals.com/wiki/index.php/ZFS_Evil_Tuning_Guide>
* <http://jrs-s.net/2015/02/03/will-zfs-and-non-ecc-ram-kill-your-data/>

