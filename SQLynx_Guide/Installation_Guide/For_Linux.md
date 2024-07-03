# Environment Check

**Mandatory Requirement**: Install JDK 1.8 or a later version.
[^Notes]:
1.SQLynx provides two versions of the software package: one with a bundled JDK and one without.
2.The version released in this repository includes a bundled JDK. If you need the version without JDK, please visit [SQLynx](https://www.sqlynx.com).
3.The JDK version released in this repository is for the AMD64 (x86) architecture. If your device uses a different architecture, you can install a suitable JDK version and choose the software package without JDK.

# Install SQLynx

## Download the Software Package
Downlaod the SQLynx software package from this repository, or visit [SQLynx](https://www.sqlynx.com).

## Startup SQLynx
### Extract the Software Package
use the unzip command in the terminal，example:
```
unzip sqlynx_linux_3.4.0.zip
```

### Startup
1.After extracting the software package, a folder named sqlynx will be generated. Execute the command,
```
cd sqlynx
```

2.Execute the ls command and you can see that there is a maicong-sqlynx.sh file in the directory.
Execute the command:
```
./maicong-sql ynx .sh
```

3.You can see three comands displayed are:
```
sh maicong-sqlynx.sh start
sh maicong-sqlynx.sh stop
sh maicong-sqlynx.sh restart
```

4.Execute the command `sh maicong-sqlynx.sh start` to start the service.

5.After startup, you can use a browser to log in to the SQLynx web page: http://<server ip address>:18888.
[^Notes]:The default port number 18888 can be customized.

6.The following login page appears, indicating that SQLynx has been installed successfully.
![SQLynx Login](https://github.com/senkae4server/-WEB_SQL_IDE-_SQLynx/blob/main/SQLynx_Guide/pics/login%20en.png)
Default username : maicong     password: setting by user’s input.

# Modify configuration
## Modify port number
1.Enter the sqlynx directory and execute the command:
```
vi config/maicong.yaml
```

2.Press the i key to enter editing mode and modify the port number.

3.Press the esc key to exit the editing mode, enter the command `:wq` to save changes and exit.

## Modify JVM heap size
1.Enter the sqlynx directory and execute the command:
```
vi config/maicong.yaml
```
2.To modify the `-Xms` and `-Xmx` parameters, which control the initial and maximum heap memory.


