# Create Security-Domain Script

JBoss/Wildfly script to create security-domain for standalone mode.


# Files

|              File              |                    Description                           |
|--------------------------------|----------------------------------------------------------|
| createSecurityDomain.cli       | Parametrized script to create security-domain            |
| enterprisecoding-sd.properties | Sample properties file for Enterprisecoding file-handler |

# Parameters

|     Parameter   |             Description                  |
|-----------------|------------------------------------------|
| securityDomain  | Name for newly declared security-domain  |
| code            | code to user for hash                    |
| username        | Username                                 |
| password        | Hashed user password                     |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createSecurityDomain.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createSecurityDomain.cli --properties=enterprisecoding-sd.properties