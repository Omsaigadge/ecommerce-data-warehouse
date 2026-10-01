\# Data base deciding









\## Questions to be asked

1. What database to be chosen for app
2. why was it chosen
3. What were the alternatives
4. disadvantages of the choice





points to be kept in mind when chooosing database for organization -- data model coverage, licensing, scalability, ecosystem maturity, and real-world adoption





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





Current leading platforms:

1. databricks -- provides tools for bi and ml, support for python, sql, scala, ml frameworks
2. snowflake -- support for structured and semi-structured data, cross cloud availability, integration is good
3. Amazon redshift -- mpp (massive parallel processing) based cloud storage, , well suited for AWS using organization
4. Amazon athena -- pay per query 
5. Dremio
6. google big query
7. Ms azure synapse analytics
8. MySQL
9. Oracel autonomous dwh
10. PostgreSQL
11. netsuite



Relational databases

1. PostgreSQL -- complex workloads -- acid compliance, advanced indexing, json and geospatial data 
2. MySQL -- fast transactional applications
3. MariaDB -- extra storage engines
4. SQLite --embedded and local storage
5. Yugabytedb -- PostgreSQL storage compatible distributed sql for scale



No sql databases

1. apache Cassandra --column store
2. redis --in-memory and key-value pair for caching and real time
3. valkey -- key value datastore
4. couchdb -- document db
5. neo4j -- graph db for high connectivity





Closed vs Open source databases

1. licensing and cost -- closed are costly and require licenses for using the software while open source are free
2. customization and flexibility -- open source has code made available which can be used for customizing as per requirement
3. community and support -- more for open source
4. transparency since code is available in open source
5. ai and vector readiness





After conclusion, we are going with open source



Licensing issues, cost required for closed applications



1\. License 

2\. SQL capabilities

3\. Data warehouse suitability

4\. Analytical features

5\. Performance/scalability characteristics

6\. Tooling/ecosystem

7\. Ease of local development



MySQL is faster and simpler for basic web and read-heavy apps, while 

PostgreSQL is more powerful and reliable for complex queries, data integrity, and write-heavy or analytical workloads





MySQL Vs Postgres Vs Maria DB



License -- dual (handles by oracle) -- community driven and free -- community driven and free

performance -- read heavy queries -- faster than MySQL -- good for massive databases

json support -- okok -- good -- best in business



!!!!!!!!!!!!!!!! POSTGRES !!!!!!!!!!!!!!!!

We have a winner



OLTP -- transactional database meant for fast row updates like upi, e-commerce where there are row updates frequently

OLAP -- where there are aggregrations, sums on extremely large datasets





**OLTP :**



Customer

&#x20;  ↓

Website

&#x20;  ↓

"Buy this phone"

&#x20;  ↓

OLTP database

&#x20;  ↓

Order created





OLAP:

CEO / Analyst

&#x20;     ↓

"What happened to phone sales?"

&#x20;     ↓

Data Warehouse

&#x20;     ↓

Millions of historical records

&#x20;     ↓

Analysis



References:

https://www.domo.com/learn/article/best-data-warehouse-platforms

https://www.instaclustr.com/education/managed-database/top-10-open-source-databases-detailed-feature-comparison/

