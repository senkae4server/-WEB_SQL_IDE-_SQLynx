## SQLynx Overview

SQLynx is a secure and efficient web-based SQL Integrated Development Environment (SQL-IDE), that supports major operating systems and databases. It features a user-friendly interface and comprehensive functionalities for database operations, especially performing well with large-scale data. SQLynx enables private deployment, with the enterprise version offering features such as permission grouping, risk rule definition, high-risk operation interception, making database management and operation safer and more convenient.

Supported Databases:
- MySQL
- Oracle
- PostgreSQL
- Hadoop
- MariaDB
- MSSQL
- SQLite

Supported Operating Systems:
- Windows
- MacOS
- Linux


## Feature Summary

1. **Database Operations**: Intelligent SQL statement suggestions, synchronous code highlighting, generation of test data and SQL statements, data import/export, data migration, table structure comparison, common code saving, database backup, and recovery.
2. **Database Audit**: User operation activity logging and analysis (reports, data visualization).
3. **Database Security Management** (Enterprise Version): Multi-user management, user access rights management, presetting and customizing risk rules for database operations, and approval management for unauthorized operations.

The release version described here is for SQLynx Pro on Linux. Installation and usage instructions apply to the Linux version. To download other versions of SQLynx software packages, please visit our website at https://www.sqlynx.com.


## Installation Guide

1. Unzip the SQLynx package and navigate to the directory using the command: `cd sqlynx`.
2. Run the command: `./maicong-sqlynx.sh`.
3. To start the service, execute: `sh maicong-sqlynx.sh start`.
4. After `maicong-sqlynx server start complete` appears, launch a web browser and enter the URL: `<Server IP Address>:18888` to access the software login screen.


## User Guide

1. For first-time users: The login username is 'maicong'. The password will be whatever the user enters in the input box and can be saved as the login password.
2. After entering the main interface, it's possible to switch between English and Chinese displays and theme colors.
3. Click the gear icon in the upper right corner to enter the data configuration page. Add the data source IP address, username, and password. Success in the test indicates successful addition of the data source.
4. Back on the main page, click refresh on the left navigation bar to see the newly added data sources. Right-clicking on different objects such as data sources, databases, and tables shows the corresponding context menu for operations.
5. Click the "+" at the top of the query window or right-click on a database name to open a new query window for SQL editing.
6. To execute multiple SQL statements simultaneously, select "Batch Execute" from the right-click menu to return multiple result sets.
7. Right-click on target data in the data viewing window for options to view, modify, delete, or export data.


## Modifying Configuration Parameters

Navigate to the sqlynx directory and execute the command: `vi config/maicong.yaml`.
1. To customize the port number, modify the value in `"server.port:18888"`.
2. To adjust the JVM heap size, modify the `"Xms JVM"` (initial heap memory) and `"Xmx JVM"` (maximum allowed heap memory) parameters.


## Resetting Password

1. Navigate to the sqlynx directory and execute: `./devops-maicong-sqlynx.sh`.
2. If 'permission denied', run: `chmod +x devops-maicong-sqlynx.sh` to add permission.
3. Upon successful execution of `./devops-maicong-sqlynx.sh`, select option `1. reset admin password`, enter the path of the SQLite.db file.
4. Enter the new password to execute.
5. A message stating “updateDateSQLiteDb password is completed” indicates a successful password reset.


## Custom Driver Packages 

(Using MySQL as an Example)
1. Navigate to the SQLynx directory and into `software/sqlynx_3.4.0/lib/mysql`. Create a new directory for the version you're using (for example, version 5.7) using the command: `mkdir 5.7`.
2. Place the corresponding database driver JAR file into the newly created folder by executing the following commands:

```
cd 5.7
cp -rf /root/mysql-connector-java-5.1.49.jar .
```
3. Launch SQLynx and go to the data source addition page. Under the 'Advanced Configuration' tab, you can now select the custom driver package from the driver dropdown list. Upon successful testing, you can successfully add the data source.


## Software Upgrade

1. Navigate to the sqlynx directory and execute: `./devops-maicong-sqlynx.sh`.
2. Add permissions if needed: `chmod +x devops-maicong-sqlynx.sh`.
3. Upon successful execution, choose option `2. historical version data migration`.
4. Enter the path of the old version sqlite.db file, the new version sqlite directory (press Enter if the default is correct), the path for initializing sqlite's .sql file, and the current version number.
5. A message stating “migration is completed” indicates a successful upgrade.
6. Verification: Launch SQLynx, log in with old credentials, and check for previously configured data sources to verify the upgrade.


## Feedback

For inquiries or feedback, please contact the SQLynx team at service@sqlynx.com.


## Software License

SQLynx Pro (Personal Edition) is available for individual users for non-commercial use free of charge. For commercial use or enterprise user purchases, please contact sales@sqlynx.com.
