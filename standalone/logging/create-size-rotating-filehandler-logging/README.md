# Create Size-Rotating File-Handler Logging Script

JBoss/Wildfly script to create size-rotating file-handler logging for standalone mode.


# Files

|              File              |                    Description                           |
|--------------------------------|----------------------------------------------------------|
| createSRFileHandlerLogging.cli   | Parametrized script to create size-rotating file-handler logging       |
| enterprisecoding-srfh.properties | Sample properties file for Enterprisecoding size-rotating file-handler |

# Parameters

|     Parameter     |                     Description                         |
|-------------------|---------------------------------------------------------|
| srfileHandlerName | Name for newly declared size-rotating file-handler  |
| loggerName        | Category name of logger                                 |
| logRelativePath   | Log file path relative to "jboss.server.log.dir"        |
| logLevel          | Log level for file-handler and logger                   |
| suffix            | Suffix used for rotated log files                       |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createSRFileHandlerLogging.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createSRFileHandlerLogging.cli --properties=enterprisecoding-srfh.properties