# Configuring MySQL Primary-Replica Model and Database Backups

In this project, I delved into configuring database servers in a primary-replica model using MySQL. The primary-replica setup enhances data redundancy, availability, and scalability by allowing read and write operations to be distributed across multiple database instances. Additionally, I created a Bash script to automate the generation of database backups, ensuring data integrity and disaster recovery preparedness.

## Configuring MySQL Primary Server

To set up the primary database server, I configured the `my.conf` configuration file as follows:

```bash
# 4-mysql_configuration_primary

[mysqld]
server-id=1
log_bin=mysql-bin
binlog_format=row
```

These configurations enable binary logging (`log_bin`) and specify the format of binary logs (`binlog_format=row`), facilitating data replication to the replica server.

## Configuring MySQL Replica Server

For the replica database server, I configured the `my.conf` configuration file as follows:

```bash
# 4-mysql_configuration_replica

[mysqld]
server-id=2
relay-log=slave-relay-bin
log_bin=mysql-bin
binlog_format=row
```

Similar to the primary server, the replica server is configured with a unique `server-id` and enables binary logging and row-based replication.

## Automating Database Backups

I developed a Bash script named `5-mysql_backup` to automate the generation of MySQL database backups. The script accepts the MySQL root password as input and performs the following tasks:

1. Connects to the MySQL server using the provided root password.
2. Generates a dump containing all MySQL databases.
3. Creates a compressed `tar.gz` archive of the dump.
4. Names the resulting archive with the current date in the format `day-month-year.tar.gz`.

Usage of the script:

```bash
./5-mysql_backup <MySQL root password>
```

This script ensures regular backups of MySQL databases, providing an essential mechanism for disaster recovery and data protection.

By configuring MySQL servers in a primary-replica model and automating database backups, I established a robust and reliable database infrastructure capable of handling data replication and ensuring data integrity and availability. These practices are essential for maintaining the stability and resilience of database systems in production environments.
