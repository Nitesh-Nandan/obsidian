👉 B+ tree force you to store the actual data in leaf Node.
👉 B+ tree make range query easier.

![[]]![[Screenshot 2023-04-15 at 10.28.51 PM.png]]

![[B+Tree.m4a]]

## Indexes

![[Screenshot 2023-04-15 at 11.06.40 PM.png]]

**Clustered vs Non-Clustered Index**
- A clustered index is an index that specifies the physical arrangement of a database's table records. There can only be one clustered index per table since there can only be one method that records are physically maintained in a database table. It stores the records in sorted order.

- A cluster index is a type of index that sorts the data rows in the table on their key values, whereas the Non-clustered index stores the data at one location and indices at another location.

- Clustered index stores data pages in the leaf nodes of the index, while the Non-clustered index method never stores data pages in the leaf nodes of the index.

- The cluster index doesn’t require additional disk space, whereas the Non-clustered index requires additional disk space.

- Cluster index offers faster data access, on the other hand, the Non-clustered index is slower.

- A Non-clustered index stores the data at one location and indices at another location. The index contains pointers to the location of that data. A single table can have many non-clustered indexes as an index in the non-clustered index is stored in different places.

### Sharding vs Partitioning

**Sharding**: Spliting a database across muliple instances.
**Partitioning**: Spliting a subset of data within same instances.

Partitioning  happens in a data label, while Sharding happens database level.

![[Screenshot 2023-04-17 at 9.16.29 PM.png]]

![[Screenshot 2023-05-07 at 2.13.23 AM.png]]
![[Screenshot 2023-05-07 at 2.13.01 AM.png]]
🤔 What will happen if partition key is globally unique?
👉 Read more: https://www.youtube.com/watch?v=ifSckJlatWE&ab_channel=TheGeekNarrator
