# Create File-Handler Logging Script

JBoss/Wildfly script to create file-handler logging for standalone mode.


# Files

|              File              |                    Description                           |
|--------------------------------|----------------------------------------------------------|
| createFileHandlerLogging.cli   | Parametrized script to create file-handler logging       |
| enterprisecoding-fh.properties | Sample properties file for Enterprisecoding file-handler |

# Parameters

|     Parameter    |                 Description                      |
|------------------|--------------------------------------------------|
| fileHandlerName  | Name for newly declared file-handler             |
| loggerName       | Category name of logger                          |
| logRelativePath  | Log file path relative to "jboss.server.log.dir" |
| logLevel         | Log level for file-handler and logger            |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createFileHandlerLogging.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createFileHandlerLogging.cli --properties=enterprisecoding-fh.properties