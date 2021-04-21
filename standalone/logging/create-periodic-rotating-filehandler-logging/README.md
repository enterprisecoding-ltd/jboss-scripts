# Create Periodic-Rotating File-Handler Logging Script

JBoss/Wildfly script to create periodic-rotating file-handler logging for standalone mode.


# Files

|              File              |                    Description                           |
|--------------------------------|----------------------------------------------------------|
| createPRFileHandlerLogging.cli   | Parametrized script to create periodic-rotating file-handler logging       |
| enterprisecoding-prfh.properties | Sample properties file for Enterprisecoding periodic-rotating file-handler |

# Parameters

|     Parameter     |                     Description                         |
|-------------------|---------------------------------------------------------|
| prfileHandlerName | Name for newly declared periodic-rotating file-handler  |
| loggerName        | Category name of logger                                 |
| logRelativePath   | Log file path relative to "jboss.server.log.dir"        |
| logLevel          | Log level for file-handler and logger                   |
| suffix            | Suffix used for rotated log files                       |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createPRFileHandlerLogging.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createPRFileHandlerLogging.cli --properties=enterprisecoding-prfh.properties