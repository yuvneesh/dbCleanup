Database Cleanup

Use Case: Certain applications have a central data storage system, i.e. all the information for the application is stored in one/set of database. Ocassionally, the size of these database might affect the performance eof application and even cause unexpected behaviour. 
For most of these applications, an empty database is provided that has the required structure but no data. In case of issues with a database, the in-use database should be archived(renamed/moved) and a blank database should be used. Some applications provide tools to do so. An alternate approach is to use a constant name for in-use database and rename when it is required to be archived followed by copying the blank database and renaming it to the constant name. 

For eg:
Application X uses a database name Records.mdb and there exit a blank database named BlankDB.mdb. In case there are issues with database, rename files as follows:
Records.mdb -> Records-DD-MM-YYY.mdb
BlankDB(Copy) -> Records.mdb

Goal: The goal of this project is allow the user to create scheduled task by defining instances of inUse/Blank database pairs. 