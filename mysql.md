mysql version
```
show variables like '%version%';
+-------------------------+------------------------------+
| Variable_name           | Value                        |
+-------------------------+------------------------------+
| innodb_version          | 5.6.51                       |
| protocol_version        | 10                           |
| slave_type_conversions  |                              |
| version                 | 5.6.51                       |
| version_comment         | MySQL Community Server (GPL) |
| version_compile_machine | x86_64                       |
| version_compile_os      | Linux                        |
+-------------------------+------------------------------+
```
### Backup
```
mysqldump -u root -p --result-file=push_chain.sql push_chain
```
### Restore
