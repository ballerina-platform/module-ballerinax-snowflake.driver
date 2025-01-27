Ballerina Snowflake Driver Library
===================

[![Build](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/workflows/CI/badge.svg)](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/actions?query=workflow%3ACI)
[![codecov](https://codecov.io/gh/ballerina-platform/module-ballerinax-snowflake.driver/branch/main/graph/badge.svg)](https://codecov.io/gh/ballerina-platform/module-ballerinax-snowflake.driver)
[![GitHub Last Commit](https://img.shields.io/github/last-commit/ballerina-platform/module-ballerinax-snowflake.driver.svg)](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/commits/master)
[![GraalVM Check](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/actions/workflows/build-with-bal-test-native.yml/badge.svg)](https://github.com/ballerina-platform/module-ballerinax-snowflake.driver/actions/workflows/build-with-bal-test-native.yml)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

[Snowflake](https://docs.snowflake.com/en/index.html) is one of the few enterprise-ready cloud data warehouses that brings simplicity without sacrificing features. It automatically scales, both up and down, to get the right balance of performance vs. cost. Snowflake’s claim to fame is that it separates compute from storage. Snowflake enables data storage, processing, and analytic solutions that are faster, easier to use, and far more flexible than traditional offerings. Snowflake provides all of the functionality of an enterprise analytic database, along with many additional special features and unique capabilities.

The Snowflake [Ballerina](https://ballerina.io/) driver library bundles the [Snowflake JDBC driver v3.14.4](https://docs.snowflake.com/en/user-guide/jdbc.html) through Ballerina. With this library, you can programmatically create and manage all Snowflake objects, including virtual warehouses, databases, and all database objects. It also provides the capability to query Snowflake data.

For more information, go to the module(s).
- [snowflake.driver](Module.md)

## Build from the source

### Set up the prerequisites

1. Download and install Java SE Development Kit (JDK) version 21 (from one of the following locations).
    * [Oracle](https://www.oracle.com/java/technologies/javase-jdk21-downloads.html)
    * [OpenJDK](https://adoptium.net/)

2.  Export your GitHub personal access token with read package permissions as follows.

        export packageUser=<Username>
        export packagePAT=<Personal access token>

### Build the source

Execute the commands below to build from the source.

1. To build the library:

        ./gradlew clean build

2.  Publish ZIP artifact to the local `.m2` repository:

        ./gradlew clean build publishToMavenLocal

3.  Publish the generated artifacts to the local Ballerina central repository:

        ./gradlew clean build -PpublishToLocalCentral=true

4. Publish the generated artifacts to the Ballerina central repository:
        
        ./gradlew clean build -PpublishToCentral=true

## Contribute to Ballerina

As an open source project, Ballerina welcomes contributions from the community.

For more information, go to the [contribution guidelines](https://github.com/ballerina-platform/ballerina-lang/blob/master/CONTRIBUTING.md).

## Code of conduct

All contributors are encouraged to read the [Ballerina code of conduct](https://ballerina.io/code-of-conduct).

## Useful links

* For more information go to the [`snowflake.driver` library](https://lib.ballerina.io/ballerinax/snowflake.driver/latest).
* Chat live with us via our [Discord server](https://discord.gg/ballerinalang).
* Post all technical questions on Stack Overflow with the [#ballerina](https://stackoverflow.com/questions/tagged/ballerina) tag.
