

# 1. Create an upload keystore

Read the official documentation to setup the keystore: https://docs.flutter.dev/deployment/android#create-an-upload-keystore

If you followed the above documentation you should end up with a local file `key.properties` (not comitted to github). This github action
will recreate that file with values inside github actions secrets, for signing the application.


# 2. Add secrets values in your repository settings

add the base64 version of your upload-keystore.jks as well as the password from the previous step in your repository actions secrets

```
base64 -i path/to/upload-keystore.jks
```
