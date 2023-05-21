- Mutiple machines to solve the problems that can't be solved by a single machine.
- for eg: Not enough storage. Too Many computation.

**Functional Requirement**
- Client a upload a large files.
- Client can donwload or Read the files.
- Client can search a files, text based search.

**Non-Functional Requirement**
- System should be highly available.
- Low Latency in downloading.
- Consistent

## FAQ

**Q. If we want to modify/update a file, how to do that?**
- GFS doesn't support the modify/update operation. So the solution is simple: we delete the old file, and write a new one(the modified one) from scratch.
- **Reason:** If the chunk becomes larger or smaller after the modification, how to handle remaining data in subsequent chunks. This will evnetually lead to rewrite-like operation

**Q. How to identify whether a chunk on the disk is broken?**
- We can calculate the checksum for each chunk and use it to detect the error.

![[hdfs.png]]

**Replication**

👉 Replication can be done via chain replication. Like consistent hashing.
👉 
![[hdfs-educative.png]]

