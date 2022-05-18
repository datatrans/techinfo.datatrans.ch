# How am I affected by certificate changes?

## Root Certificate Trust Store

Please check if you trust our root certificates.

| Certificate Authority | Root Certificate |
| :--- | :--- |
| Comodo AddTrust External CA Root | [https://support.sectigo.com/Com\_KnowledgeDetailPage?Id=kA01N000000rgSZ](https://support.sectigo.com/Com_KnowledgeDetailPage?Id=kA01N000000rgSZ) |
| DigiCert Global Root CA | [https://dl.cacerts.digicert.com/DigiCertGlobalRootCA.crt](https://dl.cacerts.digicert.com/DigiCertGlobalRootCA.crt) |

## Certificate Pinning

If you pin our certificate, you should replace the existing certificate. Certificate pinning has some downsides, as the certificate rotation will occur on a regular basis in the future and you would need to update the certificates embedded within your application accordingly.

Datatrans strongly advise **against** certificate pinning. Please contact us at [techinfo@datatrans.ch](mailto:techinfo@datatrans.ch) if you're currently using or plan to implement it.

## Public Key Pinning

If you extracted the public key from our certificate, please check our public key with the embedded copy of your applications public key. Our public key did not change since 2017. If you use our Mobile Library, please ensure that you use **at least Version 1.7.1 for Android or Version 2.1.0 for iOS**.

We do not advise to use public key pinning. Please contact us at [techinfo@datatrans.ch](mailto:techinfo@datatrans.ch) if you're currently using or plan to implement it.

