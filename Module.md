## Overview
This is a Ballerina library for [Snowflake JDBC Driver v3.13.6](https://docs.snowflake.com/en/user-guide/jdbc.html). 
The Snowflake JDBC driver is a JDBC type 4 driver that supports the core JDBC functionality in version 1.0 of the JDBC API.
You can create and manage all Snowflake objects, including virtual warehouses, databases, and all database objects. 
It also provides the capability to query Snowflake data. You can find reference information for all the Snowflake SQL commands (DDL, DML, and query syntax) [here](https://docs.snowflake.com/en/sql-reference-commands.html). You can find reference information for the system-defined SQL functions [here](https://docs.snowflake.com/en/sql-reference-functions.html).

## Prerequisites

Before using this connector in your Ballerina application, complete the following:

* Create a [Snowflake](https://www.snowflake.com) account
* Obtain the JDBC driver connection string, username and password by following [this guide](https://docs.snowflake.com/en/user-guide/jdbc-configure.html)
 
## Quickstart

To use the Snowflake driver library in your Ballerina application, update the .bal file as follows:

### Step 1: Import driver
First, import the following modules into the Ballerina project.
```ballerina
import ballerina/sql;
import ballerinax/java.jdbc;
import ballerinax/snowflake.driver as _;
```

### Step 2: Create a new connector instance
Provide the JDBC URL, username, password, optional properties and initialize the JDBC client connector with it. 
You can find more information [here](https://docs.snowflake.com/en/user-guide/jdbc-configure.html#label-other-jdbc-connection-string-examples).
```ballerina
jdbc:Options options = {
    properties: {
        warehouse: "<WAREHOUSE>",
        db: "<DATABASE>",
        schema: "<SCHEMA>"
    }
};
string jdbcUrl = "jdbc:snowflake://<ACCOUNT_IDENTIFIER>.snowflakecomputing.com";
string user = "<USERNAMR>";
string password = "<PASSWORD>";

jdbc:Client baseClient = check new (jdbcUrl, user, password, options = options);
```

### Step 3: Invoke connector operation
1. Now you can use the Ballerina JDBC client connector to consume the Snowflake API.

    Following is an example on how to verify the version of the driver you are currently using. 

    Verify your driver version

    ```ballerina
    public function main() {
        sql:ParameterizedQuery sqlQuery = `SELECT CURRENT_CLIENT()`;
        stream <record {}, sql:Error> resultStream = baseClient->query(sqlQuery);
        record {|record {} value;|}|error? result = resultStream.next();
        if result is record {|record {} value;|} {
            io:println("Current driver version: ", result.value);
        }
    }
    ``` 

    Following is an example on how to verify the warehouse, database, and schema you are currently using. 

    Verify the warehouse, database, and schema

    ```ballerina
    public function main() {
        sql:ParameterizedQuery sqlQuery = `SELECT CURRENT_WAREHOUSE(), CURRENT_DATABASE(), CURRENT_SCHEMA()`;
        stream <record {}, sql:Error> resultStream = baseClient->query(sqlQuery);
        record {|record {} value;|}|error? result = resultStream.next();
        if result is record {|record {} value;|} {
            io:println("Current details: ", result.value);
        }
    }
    ``` 

    Following is an example on how to query data from a table called `DEMO`. 

    Query the data

    ```ballerina
    public function main() {
        sql:ParameterizedQuery sqlQuery = `SELECT * FROM DEMO`;
        stream <record {}, sql:Error> resultStream = baseClient->query(sqlQuery);

        error? e = resultStream.forEach(isolated function(record {} result) {
            io:println("Current query details: ", result);
        });
    }
    ``` 

2. Use `bal run` command to compile and run the Ballerina program.
