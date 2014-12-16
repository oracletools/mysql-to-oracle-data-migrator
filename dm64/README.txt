##
##dm64.exe -h ALL 

----------------------------------------------------------------------
MySQL to Oracle DataMigrator (v1.23.9, beta, 2014/12/16 09:36:33) [64bit]
Copyright (c): 2014 Alex Buzunov, All rigts reserved.
Agreement: Use this tool at your own risk. Author is not liable for any damages or losses related to the use of this software.
----------------------------------------------------------------------
From MySQL:

Set following command line arguments to copy from MySQL to Oracle:

-w copy_vector -o pool_size -r num_of_shards -t field_term -l lame_duck -K keep_data_file -1 arg_1 -2 arg_2 -3 arg_3 -q query_sql_file -Q query_sql_dir -c from_table -P from_partition -S from_sub_partition -j from_user -x from_passwd -b from_db_name -n from_db_server -z source_client_home -g to_db -a to_table -e nls_date_format -m nls_timestamp_format -O nls_timestamp_tz_format -Z target_client_home 

Here:
(Common) -w [--copy_vector]	Data copy direction.	
(Common) -o [--pool_size]	Pool size.	
(Common) -r [--num_of_shards]	Number of shards.	
(Common) -t [--field_term]	Field terminator.	
(Common) -l [--lame_duck]	Limit rows (lame duck run).	
(Common) -K [--keep_data_file]	Keep data dump.	
(Common) -1 [--arg_1]	Generic string argument 1.	
(Common) -2 [--arg_2]	Generic string argument 2.	
(Common) -3 [--arg_3]	Generic string argument 3.	
(From MySQL) -q [--query_sql_file]	Input file with MySQL query sql.	
(From MySQL) -Q [--query_sql_dir]	Input file with MySQL query sql.	
(From MySQL) -c [--from_table]	From table.	
(From MySQL) -P [--from_partition]	From partition.	
(From MySQL) -S [--from_sub_partition]	From sub-partition.	
(From MySQL) -j [--from_user]	MySQL source user.	
(From MySQL) -x [--from_passwd]	MySQL source user password.	
(From MySQL) -b [--from_db_name]	MySQL source database.	
(From MySQL) -n [--from_db_server]	MySQL source instance name.	
(From MySQL) -z [--source_client_home]	Path to MySQL client home.	
(To Oracle) -g [--to_db]	To Oracle database.	
(To Oracle) -a [--to_table]	To Oracle table.	
(To Oracle) -e [--nls_date_format]	nls_date_format for target.	
(To Oracle) -m [--nls_timestamp_format]	nls_timestamp_format for target.	
(To Oracle) -O [--nls_timestamp_tz_format]	nls_timestamp_tz_format for target.	
(To Oracle) -Z [--target_client_home]	Path to Oracle client home bin dir.	

--USE CASES--

1. MySQL_to_Oracle. 16 use cases.


MySQL_to_Oracle: 16 use case(s) available:

1. MYSQL_Partition_Limit22_to_ORA_Table - Copy only 22 rows from MySQL partition into Oracle Table table.
2. MYSQL_Partition_to_ORA_Table - Copy MySQL partition into Oracle Table table.
3. MYSQL_QueryDir_Limit333_to_ORA_Table - Read each SQL query file from a directory "c:\Python27\data_migrator_1239\test\v101\query\query_dir_mysql".
	  Copy only 333 rows from MySQL query results into Oracle Table table.
4. MYSQL_QueryDir_to_ORA_Table - Read each SQL query file from a directory "c:\Python27\data_migrator_1239\test\v101\query\query_dir_mysql".
	  Copy MySQL query results into Oracle Table table.
5. MYSQL_QueryFile_Limit100_to_ORA_Table - Read SQL from a query file "c:\Python27\data_migrator_1239\test\v101\query\mysql_query.sql".
	  Copy only 100 rows from MySQL query results into Oracle Table table.
6. MYSQL_QueryFile_to_ORA_Table - Read SQL from a query file "c:\Python27\data_migrator_1239\test\v101\query\mysql_query.sql".
	  Copy MySQL query results into Oracle Table table.
7. MYSQL_ShardedPartition_to_ORA_Table - Break input sharded partition into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL sharded partition into Oracle Table table.
8. MYSQL_ShardedQuery_to_ORA_Table - Break input query results into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL query results into Oracle Table table.
9. MYSQL_ShardedSubpartition_to_ORA_Table - Break input sharded sub-partition into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL sharded sub-partition into Oracle Table table.
10. MYSQL_ShardedTable_to_ORA_Table - Break input table into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL table into Oracle Table table.
11. MYSQL_Subpartition_Limit33_to_ORA_Table - Copy only 33 rows from MySQL sub-partition into Oracle Table table.
12. MYSQL_Subpartition_to_ORA_Table - Copy MySQL sub-partition into Oracle Table table.
13. MYSQL_Table_KeepSpoolFile_to_ORA_Table - Copy MySQL table into Oracle Table table.
14. MYSQL_Table_Limit1000_to_ORA_Table - Copy only 1000 rows from MySQL table into Oracle Table table.
15. MYSQL_Table_to_ORA_Table - Copy MySQL table into Oracle Table table.
16. MYSQL_TimezoneQueryFile_to_ORA_Table - Read SQL from a query file "c:\Python27\data_migrator_1239\test\v101\query\mysql_query_tz_to_ora.sql".
	  Copy MySQL query results into Oracle Table table.

--DETAILS--

-USE-CASE # 1
Use case name: MYSQL_Partition_Limit22_to_ORA_Table
	Description:  Copy only 22 rows from MySQL partition into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -l[--lame_duck] is "Limit rows (lame duck run)."
  -c[--from_table] is "From table."
  -P[--from_partition] is "From partition."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -l 22 ^
  -c TEST.Partitioned_test_from ^
  -P rx2015 ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 2
Use case name: MYSQL_Partition_to_ORA_Table
	Description:  Copy MySQL partition into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -c[--from_table] is "From table."
  -P[--from_partition] is "From partition."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -c TEST.Partitioned_test_from ^
  -P rx2015 ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 3
Use case name: MYSQL_QueryDir_Limit333_to_ORA_Table
	Description:  Read each SQL query file from a directory "c:\Python27\data_migrator_1239\test\v101\query\query_dir_mysql".
	  Copy only 333 rows from MySQL query results into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -l[--lame_duck] is "Limit rows (lame duck run)."
  -Q[--query_sql_dir] is "Input file with MySQL query sql."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -l 333 ^
  -Q c:\Python27\data_migrator_1239\test\v101\query\query_dir_mysql ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 4
Use case name: MYSQL_QueryDir_to_ORA_Table
	Description:  Read each SQL query file from a directory "c:\Python27\data_migrator_1239\test\v101\query\query_dir_mysql".
	  Copy MySQL query results into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -Q[--query_sql_dir] is "Input file with MySQL query sql."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -Q c:\Python27\data_migrator_1239\test\v101\query\query_dir_mysql ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 5
Use case name: MYSQL_QueryFile_Limit100_to_ORA_Table
	Description:  Read SQL from a query file "c:\Python27\data_migrator_1239\test\v101\query\mysql_query.sql".
	  Copy only 100 rows from MySQL query results into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -l[--lame_duck] is "Limit rows (lame duck run)."
  -q[--query_sql_file] is "Input file with MySQL query sql."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -l 100 ^
  -q c:\Python27\data_migrator_1239\test\v101\query\mysql_query.sql ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 6
Use case name: MYSQL_QueryFile_to_ORA_Table
	Description:  Read SQL from a query file "c:\Python27\data_migrator_1239\test\v101\query\mysql_query.sql".
	  Copy MySQL query results into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -q[--query_sql_file] is "Input file with MySQL query sql."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -q c:\Python27\data_migrator_1239\test\v101\query\mysql_query.sql ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 7
Use case name: MYSQL_ShardedPartition_to_ORA_Table
	Description:  Break input sharded partition into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL sharded partition into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -c[--from_table] is "From table."
  -P[--from_partition] is "From partition."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 3 ^
  -r 3 ^
  -t "|" ^
  -c TEST.Partitioned_test_from ^
  -P rx2015 ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 8
Use case name: MYSQL_ShardedQuery_to_ORA_Table
	Description:  Break input query results into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL query results into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -q[--query_sql_file] is "Input file with MySQL query sql."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 3 ^
  -r 3 ^
  -t "|" ^
  -q c:\Python27\data_migrator_1239\test\v101\query\mysql_query.sql ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 9
Use case name: MYSQL_ShardedSubpartition_to_ORA_Table
	Description:  Break input sharded sub-partition into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL sharded sub-partition into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -c[--from_table] is "From table."
  -S[--from_sub_partition] is "From sub-partition."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 3 ^
  -r 3 ^
  -t "|" ^
  -c TEST.Sub_Partitioned_test_from ^
  -S subpart200 ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 10
Use case name: MYSQL_ShardedTable_to_ORA_Table
	Description:  Break input table into 3 logical shards (-r[--num_of_shards] 3) 
	  and run copy process on each shard in thread pool (-o[--pool_size] 3).
	  Copy MySQL table into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -c[--from_table] is "From table."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 3 ^
  -r 3 ^
  -t "|" ^
  -c TEST.Timestamp_test_from ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 11
Use case name: MYSQL_Subpartition_Limit33_to_ORA_Table
	Description:  Copy only 33 rows from MySQL sub-partition into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -l[--lame_duck] is "Limit rows (lame duck run)."
  -c[--from_table] is "From table."
  -S[--from_sub_partition] is "From sub-partition."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -l 33 ^
  -c TEST.Sub_Partitioned_test_from ^
  -S subpart200 ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 12
Use case name: MYSQL_Subpartition_to_ORA_Table
	Description:  Copy MySQL sub-partition into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -c[--from_table] is "From table."
  -S[--from_sub_partition] is "From sub-partition."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -c TEST.Sub_Partitioned_test_from ^
  -S subpart200 ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 13
Use case name: MYSQL_Table_KeepSpoolFile_to_ORA_Table
	Description:  Copy MySQL table into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -K[--keep_data_file] is "Keep data dump."
  -c[--from_table] is "From table."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -K 1 ^
  -c TEST.Timestamp_test_from ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 14
Use case name: MYSQL_Table_Limit1000_to_ORA_Table
	Description:  Copy only 1000 rows from MySQL table into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -l[--lame_duck] is "Limit rows (lame duck run)."
  -c[--from_table] is "From table."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -l 1000 ^
  -c TEST.Timestamp_test_from ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 15
Use case name: MYSQL_Table_to_ORA_Table
	Description:  Copy MySQL table into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -c[--from_table] is "From table."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -c TEST.Timestamp_test_from ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timestamp_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"

-USE-CASE # 16
Use case name: MYSQL_TimezoneQueryFile_to_ORA_Table
	Description:  Read SQL from a query file "c:\Python27\data_migrator_1239\test\v101\query\mysql_query_tz_to_ora.sql".
	  Copy MySQL query results into Oracle Table table.
	Arguments:
	  -w[--copy_vector] is "Data copy direction."
  -o[--pool_size] is "Pool size."
  -r[--num_of_shards] is "Number of shards."
  -t[--field_term] is "Field terminator."
  -q[--query_sql_file] is "Input file with MySQL query sql."
  -j[--from_user] is "MySQL source user."
  -x[--from_passwd] is "MySQL source user password."
  -b[--from_db_name] is "MySQL source database."
  -n[--from_db_server] is "MySQL source instance name."
  -z[--source_client_home] is "Path to MySQL client home."
  -g[--to_db] is "To Oracle database."
  -a[--to_table] is "To Oracle table."
  -e[--nls_date_format] is "nls_date_format for target."
  -m[--nls_timestamp_format] is "nls_timestamp_format for target."
  -O[--nls_timestamp_tz_format] is "nls_timestamp_tz_format for target."
  -Z[--target_client_home] is "Path to Oracle client home bin dir."	
	Example: 
	  echo y|c:\Python27\dm_dist_64\20141216_093633\dm64\dm64.exe ^
  -w mysql2ora ^
  -o 1 ^
  -r 1 ^
  -t "|" ^
  -q c:\Python27\data_migrator_1239\test\v101\query\mysql_query_tz_to_ora.sql ^
  -j "alex" ^
  -x "mysql_pwd" ^
  -b "test" ^
  -n "localhost" ^
  -z "C:\Temp\mysql\bin" ^
  -g SCOTT/tiger2@orcl ^
  -a SCOTT.Timezone_test_to ^
  -e "YYYY-MM-DD HH24.MI.SS" ^
  -m "YYYY-MM-DD HH24.MI.SS.FF2" ^
  -O "YYYY-MM-DD HH:MI:SS.FF2 TZH:TZM" ^
  -Z "C:\app\alex_buz\product\11.2.0\dbhome_2\BIN"