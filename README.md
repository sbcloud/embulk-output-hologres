# embulk-output-hologres
 This file output plugin is used to write records to Aliyun hologres
,Hologres output plugin for Embulk can loads records to hologres by using embulk-output-postgresql plugin.

## Overview

* **Plugin type**: output
* **Load all or nothing**: no
* **Resume supported**: yes
* **Cleanup supported**: yes

## Configuration

- **host**: host name-hologres Public Network endpoint(string,required)
- **port**: hologres port number (integer, default: 80)
- **user**: Aliyun account accessKeyId (string, required)
- **password**: Aliyun account accessKeySecret (string, required)
- **database**: destination database name (string, required)
- **table**: destination table name (string, required)
- **mode**: insert_direct,INSERT in transaction is not supported now

 cf.https://github.com/embulk/embulk-output-jdbc/blob/master/embulk-output-postgresql/README.md

## Example

```yaml
out:
  type: postgresql
  host: hgpost-sg-yv71ti7z2003-ap-southeast-1.hologres.aliyuncs.com
  port: 80
  user: accessKeyId
  password: "accessKeySecret"
  database: polodw
  table: test1_demo2
  mode: insert_direct
``` 

## Build

```
$ ./gradlew gem  
```