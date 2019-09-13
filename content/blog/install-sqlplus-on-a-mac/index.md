---
title: "Install SQL*Plus 12.2 on a Mac"
date: 2019-06-07T13:06:55-05:00
tags: [mac, sqlplus, sql]
toc: false
show_comments: true
---

1. Navigate to [Oracle downloads](https://www.oracle.com/technetwork/topics/intel-macsoft-096467.html), accept the license agreement, and login. If you don't already have an Oracle account, you'll need to create one
1. Download these zip files:
    1. `instantclient-basic-macos.x64-12.2.0.1.0-2.zip`
    1. `instantclient-sqlplus-macos.x64-12.2.0.1.0-2.zip`
1. Run `mkdir -p ~/bin/instantclient_12_2`
1. Unzip the contents of both zip files directly into `~/bin/instantclient_12_2`. The file listing should look like:
    ```
    $ find . | sort
    .
    ./BASIC_README
    ./SQLPLUS_README
    ./adrci
    ./genezi
    ./glogin.sql
    ./libclntsh.dylib
    ./libclntsh.dylib.12.1
    ./libclntshcore.dylib.12.1
    ./libnnz12.dylib
    ./libocci.dylib
    ./libocci.dylib.12.1
    ./libociei.dylib
    ./libocijdbc12.dylib
    ./libons.dylib
    ./liboramysql12.dylib
    ./libsqlplus.dylib
    ./libsqlplusic.dylib
    ./ojdbc8.jar
    ./sqlplus
    ./uidrvci
    ./xstreams.jar
    ```
1. Add this line to your `~/.bash_profile`
    ```
    export PATH="$PATH:$HOME/bin/instantclient_12_2"
    ```
1. Run `source ~/.bash_profile`
1. Run `sqlplus -V` to confirm it's installed 