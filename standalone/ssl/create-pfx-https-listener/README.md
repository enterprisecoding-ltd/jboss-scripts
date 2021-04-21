# Create Https Listener - PKCS#12 (pfx)

JBoss/Wildfly script to create https listener using PKCS#12 (pfx) keystore for standalone mode.


# Files

|                File         |                       Description                       |
|-----------------------------|---------------------------------------------------------|
| createPFXHttpsListener.cli  | Parametrized script to create HTTPS listener using pfx  |
| pfx-https.properties        | Sample properties file                                  |

# Parameters

| Parameter   |      Description      |
|-------------|-----------------------|
| realmName   | Realm name to create  |
| pfxPath     | Key store path        |
| pfxPassword | Key store password    |

## Usage

Create or edit properties file with desired values, then execute following command;

    ./jboss-cli.sh -c --file=createPFXHttpsListener.cli --properties=[PROPERTIES FILE] 

> **Note**: Replace **[PROPERTIES FILE]** with your properties file

Example;

    ./jboss-cli.sh -c --file=createPFXHttpsListener.cli --properties=pfx-https.properties