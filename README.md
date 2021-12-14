Ballerina Snowflake Driver Library
===================

[![Build](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/workflows/CI/badge.svg)](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/actions?query=workflow%3ACI)
[![GitHub Last Commit](https://img.shields.io/github/last-commit/ballerina-platform/module-ballerinax-snowflake.driver.svg)](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/commits/master)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

[Snowflake](https://docs.snowflake.com/en/index.html) is one of the few enterprise-ready cloud data warehouses that brings simplicity without sacrificing features. It automatically scales, both up and down, to get the right balance of performance vs. cost. Snowflake’s claim to fame is that it separates compute from storage. Snowflake enables data storage, processing, and analytic solutions that are faster, easier to use, and far more flexible than traditional offerings. Snowflake provides all of the functionality of an enterprise analytic database, along with many additional special features and unique capabilities.

The Snowflake [Ballerina](https://ballerina.io/) driver library bundles the [Snowflake JDBC driver v3.13.6](https://docs.snowflake.com/en/user-guide/jdbc.html) through Ballerina. With this library, you can programmatically create and manage all Snowflake objects, including virtual warehouses, databases, and all database objects. It also provides the capability to query Snowflake data.

For more information, go to the module(s).
- [snowflake.driver](Module.md)

## Building from the source

### Setting up the prerequisites

1. Download and install Java SE Development Kit (JDK) version 11. You can install either [OpenJDK](https://adoptopenjdk.net/) or [Oracle](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

    > **Note:** Set the JAVA_HOME environment variable to the path name of the directory into which you installed JDK.

2. Download and install [Ballerina Swan Lake](https://ballerina.io/). 

### Building the source

Execute the commands below to build from the source.

- To build the package:
    ```shell
    bal pack
    ```
- To run tests after build: 
    ```shell
    bal test
    ```

## Contributing to Ballerina

As an open source project, Ballerina welcomes contributions from the community. 

For more information, go to the [contribution guidelines](https://github.com/ballerina-platform/ballerina-lang/blob/master/gsheet/CONTRIBUTING.md).

## Code of conduct

All the contributors are encouraged to read the [Ballerina Code of Conduct](https://ballerina.io/code-of-conduct).

## Useful links

* Discuss the code changes of the Ballerina project in [ballerina-dev@googlegroups.com](mailto:ballerina-dev@googlegroups.com).
* Chat live with us via our [Slack channel](https://ballerina.io/community/slack/).
* Post all technical questions on Stack Overflow with the [#ballerina](https://stackoverflow.com/questions/tagged/ballerina) tag.
