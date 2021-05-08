# Create Https Listener

JBoss/Wildfly script to create https listener for standalone mode.


# Files

|                File              |                       Description                           |
|----------------------------------|-------------------------------------------------------------|
| createKeyStoreHttpsListener.cli  | Parametrized script to create HTTPS listener using keystore |
| keystore-https.properties        | Sample properties file                                      |

# Parameters

|     Parameter    |          Description          |
|------------------|-------------------------------|
| realmName        | Realm name to create          |
| keystorePath     | Key store path                |
| keystorePassword | Key store password            |
| keyPassword      | Key password                  |
| alias            | Certificate alias             |
| profile          | profile to add https-listener |
| server           | server to add https-listener  |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createKeyStoreHttpsListener.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createKeyStoreHttpsListener.cli --properties=keystore-https.properties