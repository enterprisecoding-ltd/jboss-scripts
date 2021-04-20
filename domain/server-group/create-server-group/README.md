# Create Server Group Script

JBoss/Wildfly script to create fserve group for domain mode.


# Files

|              File              |                    Description                           |
|--------------------------------|----------------------------------------------------------|
| createServerGroup.cli   | Parametrized script to create server group       |
| enterprisecoding-sg.properties | Sample properties file for Enterprisecoding server group |

# Parameters

|      Parameter      |                 Description                   |
|---------------------|-----------------------------------------------|
| serverGroupName     | Name for newly declared server group          |
| profileName         | Profile name to use with server group         |
| socketBindingGroup  | Socket binding group to use with server group |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createServerGroup.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createServerGroup.cli --properties=enterprisecoding-sg.properties