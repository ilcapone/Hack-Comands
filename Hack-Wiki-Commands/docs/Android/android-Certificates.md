# Inspect Certificate

## Inspect Certificate previusly extract with Apktool
```openssl pkcs7 -inform DER -in [Cert.rsa] -noout -print_certs -text```

## Less Android SDK for manipulate installing certificate trusted

In order to install a certificate on the device and for it to be validated for HTTPS connections, it is necessary that the android API version is lower than 11.

https://httptoolkit.tech/blog/android-11-trust-ca-certificates/
