# androidPublicKeyExtractor

Extracts the public keys from keystores defined by the app's signing configurations
 
This is useful when these public keys of an app's certificates need to be inserted into other consumer applications for verification purposes.

## Usage

```groovy
apply from: 'https://raw.githubusercontent.com/balazsbanyai/androidPublicKeyExtractor/master/publicKeyExtractor.gradle'
```

Then run ```./gradlew tasks``` and observe that the extract tasks are created for each signing config:

```
Public key extractor tasks
--------------------------
extractPublicKeyFromReleaseSign - extracts the public key from the ReleaseSign signing configuration
extractPublicKeyFromLocalDevSign - extracts the public key from the LocalDevSign signing configuration
extractPublicKeys - extracts the public keys from all signing configurations
```

After running the desired task, observe the project/build/publicKeys folder for the results.

```
.
└── app
    └── build
        └── publicKeys
            └──localdevsign.keystore.publicKey

```