\# Data base deciding









\## Questions to be asked

1. What database to be chosen for app
2. why was it chosen
3. What were the alternatives
4. disadvantages of the choice



\## Points to keep in mind while deciding

1. performance and workload handling

   1. complex sql queries
   2. large joins
   3. analytics workload
   4. high concurrency
   5. streaming ingestion
   6. ai-driven data processing
   7. query latency
   8. caching 
   9. behaviour
   10. handling workload of multiple working teams
2. storage and compute separation

   1. storage -- what is storage -- actual physical or cloud disks where data is stored, it acts as ssot and ensures saves and backups -- examples : amazon s3, azure blob, local db disk spaces
3. compute --  what is compute -- cpu and memory ram used to query results, it does sql queries, joins, filter records, -- examples: vm
4. pricing model -- pricing is done on various factors

   1. storage -- actual physical storage
   2. compute -- query joins and operations on the data
   3. data egress -- flow of data to external systems
   4. concurrency -- multiple users read and write at the same time on the data
5. ecosystem and integrations
6. governance and security -- rbac, compliance when applicable, column level lineage, data masking, 
7. multicloud and hybrid support -- on-prem support for multi cloud and db systems
8. ai and advanced analytics support





References:

https://www.domo.com/learn/article/best-data-warehouse-platforms

