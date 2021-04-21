# Create Server Group Script

JBoss/Wildfly script to create fserve group for domain mode.


# Files

|              File               |                    Description                          |
|---------------------------------|---------------------------------------------------------|
| addServerToGroup.cli            | Parametrized script to add a server to a server group   |
| enterprisecoding-s2g.properties | Sample properties file                                  |

# Parameters


|      Parameter      |       Description                |
|---------------------|----------------------------------|
| hostName            | Hostname to add server           |
| serverName          | Server name                      |
| serverGroupName     | Server group name to add server  |
| portOffset          | Port offset used for the server  |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=addServerToGroup.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=addServerToGroup.cli --properties=enterprisecoding-s2g.properties