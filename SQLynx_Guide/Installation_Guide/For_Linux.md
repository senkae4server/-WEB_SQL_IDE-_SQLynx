# 1. Environment Check

Please check if JDK is installed on your computer and verify the installed version by using the command `java -version`

**Requirement**: Install `JDK 1.8 or a later version`.

**Notes**:

-SQLynx offers two versions of software packages，one includes the JDK, while the other does not.

-The package released in this repository with `JDK version 1.8` and `AMD64 (X86)` architecture.

-If you need a different version of JDK, or if your computer uses a different architecture, you can install a suitable JDK version and choose the software package `without JDK`.

-If you need packages for `Windows` or `macOS`, please visit [SQLynx](https://www.sqlynx.com) to download them.


# 2. Install SQLynx
## **2.1. Download Software Package**

Downlaod the SQLynx software package from this repository, or visit [SQLynx](https://www.sqlynx.com).

## **2.2. Startup SQLynx**

2.2.1 Extract the Software Package

Use the unzip command in the terminal:`unzip sqlynx_linux_3.4.0.zip`

2.2.2 Startup

-After extracting the software package, a folder named sqlynx will be generated. Execute the command: `cd sqlynx`

-Execute the `ls` command and you can see that there is a `maicong-sqlynx.sh` file in the directory.
Execute the command:`./maicong-sql ynx .sh`

-You can see three comands displayed are:
```
sh maicong-sqlynx.sh start
sh maicong-sqlynx.sh stop
sh maicong-sqlynx.sh restart
```

-Execute the command `sh maicong-sqlynx.sh start` to start the service.

-After startup, you can use a browser to log in to the SQLynx web page: `http://<server ip address>:18888.`

**Notes**:The default port number `18888` can be customized.

-The following login page appears, indicating that SQLynx has been installed successfully.

![SQLynx Login](https://github.com/senkae4server/-WEB_SQL_IDE-_SQLynx/assets/173672207/36d6dd7a-d82e-4742-a310-515759fcea5d)


Default username :`maicong`;     Password is `setting by user’s input`.

# 3. Modify configuration

## **3.1 Modify port number**

-Enter the sqlynx directory and execute the command:`vi config/maicong.yaml`

-Press the `i key` to enter editing mode and modify the `port number`.

-Press the `esc key` to exit the editing mode, enter the command `:wq` to save changes and exit.

## **3.2 Modify JVM heap size**

-Enter the sqlynx directory and execute the command:`vi config/maicong.yaml`

-To modify the `-Xms` and `-Xmx` parameters, which control the initial and maximum heap memory.


