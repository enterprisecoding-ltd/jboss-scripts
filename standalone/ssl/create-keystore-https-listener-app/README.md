# Create Https Listener - App

JBoss/Wildfly script to create https listener on standalone mode for a single application.


# Files

|                  File               |                       Description                           |
|-------------------------------------|-------------------------------------------------------------|
| createAppKeyStoreHttpsListener.cli  | Parametrized script to create HTTPS listener using keystore |
| app-keystore-https.properties       | Sample properties file                                      |

# Parameters

|     Parameter    |          Description          |
|------------------|-------------------------------|
| realmName        | Realm name to create          |
| keystorePath     | Key store path                |
| keystorePassword | Key store password            |
| keyPassword      | Key password                  |
| alias            | Certificate alias             |
| serverName       | Secure server name to create  |
| hostName         | Secure hostname to create     |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createAppKeyStoreHttpsListener.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createAppKeyStoreHttpsListener.cli --properties=app-keystore-https.properties