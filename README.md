# SSHCONNECT

## Before using
-----------
Before run sshconnect script, you need to install a few libs: **jq** and **expect**.
```
    sudo apt install jq
    sudo apt install expect
```

## JSON
-----------
After install needed libs, you must to copy [hosts_example.json](https://github.com/Frynode/sshconnect/blob/main/json/hosts_example.json) into the same directory, rename to **hosts.json** and fill him your data.
This file contains your list of hosts and data, witch needed to connection (name, IP-address, port, user, password).<br/>
Structure of JSON file is given below:
```JSON
    "hosts":
        [
            {
                "name": "test1",
                "user": "root",
                "host": "123.123.123.123",
                "port": "22",
                "password": "qwerty123"
            },
            {
                "name": "test2",
                "user": "root",
                "host": "123.123.123.123",
                "port": "22",
                "password": "qwerty123"
            }
        ]
```
After creating **hosts.json** you can use this script.

## Basic usage
-----------
Write in terminal
```
    sshconnect hostname
```
Script will be look your JSON file and trying to find needed hostname. If he can find someone - will be init ssh connection with data from file.<br/>
Password will be pasting automatically.<br/>
After few seconds you will be connect to this host.