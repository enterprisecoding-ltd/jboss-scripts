# Create DataSource Script

JBoss/Wildfly script to create datasource for standalone mode.


# Files

|          File         |                 Description                      |
|-----------------------|--------------------------------------------------|
| createDataSource.cli  | Parametrized script to create datasource         |
| mysql.properties      | Sample properties file for MySQL datasource      |
| oracle-xe.properties  | Sample properties file for Oracle XE datasource  |
| postgresql.properties | Sample properties file for PostgreSQL datasource |


## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createDataSource.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createDataSource.cli --properties=mysql.properties