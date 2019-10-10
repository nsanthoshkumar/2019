# Demystifying SQL(DB2)

There are three types of Query Languages, DDL, DML, DCL

Two types of DataTypes:
1. Built-in DataTypes
2. User defined DataTypes
    * User-defined distinct datatypes
    * User-defined structure datatypes--> to promote OOP concepts in relational.
    * User-defined reference datatypes

Three types of Tables 
 1. Permanent(base)
 2. Temporary(Declared)
 3. Temporary(Derived)

* TableSpace :
   1. SMS: By default the following 3 are created
         * USERSPACE1
         * TEMPSPACE1 - temp tables
         * SYSCATSPACE - system catalog tables
   2. DMS: Database managed space
* Schemas : Tables created without schema name are created in Authorization UserId.
* Views : Views can be updated if they are simple 
* Buffer Pools: Buffer pools are used to cache the data pages in memory. Once the page is placed in buffer pool,
  querying to disk will be avoided.

   DEFAULTBP is the default buffer pool created whenever a database is created.
   CREATE BUFFERPOOL is used to create buffer pool. Later, a table space can be assigned to the buffer pool. 
   SYSCAT.BUFFERPOOLS to access the buffer pools defined in database

   `Question: Creating multiple buffer pools and assigning multiple table spaces to different buffer pools will increase the       performance?`

* Transactions(Unit of Work)
* Locks : Multiuser database. Locking strategy is specified by `isolation level` when binding the application
   1. Table Locks
   2. Row Locks
  Locks are stored in memory on the server as locklist.
 * Log files : Uses write ahead logging meaning first writes to the log and then later persists to the database tables.
 
 
