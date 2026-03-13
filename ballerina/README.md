## Overview

The Snowflake driver provides a reliable and high-performance connectivity to Snowflake data warehouses. It enables efficient execution of SQL queries, updates, and other database operations. The driver is designed to provide a seamless experience for interacting with Snowflake, supporting various data types and advanced features of the data warehouse.

### Key Features

- High-performance and reliable database connectivity\n- Support for various SQL operations (Query, Execute, Batch)\n- Efficient handling of database connections and resources\n- Support for database-specific data types and features\n- Secure communication with TLS and authentication\n- GraalVM compatible for native image builds

## Package overview
This Package bundles the latest Snowflake driver so that the Snowflake connector can be used in ballerina projects easily.

## Compatibility

| |  Version   |
|:---|:----------:|
|Snowflake Driver | **3.14.4** |

> The above Snowflake drivers are released under the [The Apache Software License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt).

## Usage

To add the Snowflake driver dependency the project, simply import the module as below,

```ballerina
import ballerina/sql;
import ballerinax/snowflake;
import ballerinax/snowflake.driver as _;
```
## Report issues
To report bugs, request new features, start new discussions, etc., go to the [Ballerina Library repository](https://github.com/ballerina-platform/ballerina-library)

## Useful links
* Chat live with us via our [Discord server](https://discord.gg/ballerinalang).
* Post all technical questions on Stack Overflow with the [#ballerina](https://stackoverflow.com/questions/tagged/ballerina) tag.
