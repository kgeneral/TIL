# From Oracle JDK 8 to OpenJDK 11

## GC Options
- https://opennms.discourse.group/t/migration-of-jvm-settings-from-oracle-jdk-8-to-openjdk-11/365
```bash
-Xlog:gc*                                              # Equivalent to PrintGCDetails
-Xlog:::time,uptime,level,tags"                        # Equivalent to PrintGCTimeStamps, Uptime and PrintGCDateStamps
-Xlog:safepoint"                                       # Print time elapsed from last pause
-Xlog:gc:/gc.log:time,uptime:filecount=4,filesize=20M" # Log to a file with logrotate

# Best practice to debug GC or Memory problem
-Xlog:gc*,gc+phases=debug:file=/opt/opennms/logs/gc.log:time,pid,tags:filecount=10,filesize=20m
```

# Check detailed infos for installed jdk

```bash
➜  ~ java -XshowSettings:properties -version
Property settings:
    file.encoding = UTF-8
...
    java.runtime.name = OpenJDK Runtime Environment
    java.runtime.version = 14.0.1+7
    java.specification.name = Java Platform API Specification
    java.specification.vendor = Oracle Corporation
    java.specification.version = 14
    java.vendor = AdoptOpenJDK
    java.vendor.url = https://adoptopenjdk.net/
    java.vendor.url.bug = https://github.com/AdoptOpenJDK/openjdk-support/issues
    java.vendor.version = AdoptOpenJDK
    java.version = 14.0.1
...
    sun.jnu.encoding = UTF-8
    sun.management.compiler = HotSpot 64-Bit Tiered Compilers
...

openjdk version "14.0.1" 2020-04-14
OpenJDK Runtime Environment AdoptOpenJDK (build 14.0.1+7)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 14.0.1+7, mixed mode, sharing)
```
