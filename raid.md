---
title: RAID levels
---

Level | Data distribution                                                       | Performance                                                                                                                             | Space availability | Redundancy
0     | Data is striped over multiple disks.                                    | Higher read/write perf, since it’s split over disks                                                                                     | All disks are available as one pool                              | None - loss of one disk is catastrophic
1     | Data is mirrored over multiple disks                                    | Read performance increased since multiple blocks can be accessed at the same time. Write perf declines since data must be written twice | Available disk is effectively halved.                                                                                                     | Loss of 1 disk is non-catastrophic
4     | Data striped over multiple disks. Parity information on a separate disk | Read operations benefit by striping. Writes are bottlenecked on the parity disk                                                         | More efficient use of data redundancy with parity disk                                        | If parity disk is lost, data redundancy is lost
5     | Data and parity striped over multiple disks                             | Read operations benefit by striping                                                                                                     |                                               | Can only handle one disk failure before data loss
6     | Data and dual parity blocks striped over multiple disks                 | Read operations benefit by striping                                                                                                     |                                               | Can handle two disk failures before data loss
10    | Hybridizing of 1 + 0, striping over mirrored sets                       | Read operations benefit by striping                                                                                                     |                                               |

