![](/assets/chain.png)

## Root Certificate Trust Store
Please check if you trust our root certificates.  

## Certificate Pinning
If you pin our certificate, you should replace the existing certificate. Certificate pinning has some downsides, as the certificate rotation will occur on a regular basis in the future and you would need to update the certificates embedded within your application accordingly. 

Datatrans strongly advise **against **certificate pinning. Please contact us at [techinfo@datatrans.ch](mailto:techinfo@datatrans.ch) if you're currently using or plan to implement it.


## Public Key Pinning
If you extracted the public key from our certificate, please check our new public key with the embedded copy of your applications public key, as this public key **has changed**. If you use our Mobile Library, please ensure that you use **at least Version 1.7.1 for Android or Version 2.1.0 for iOS**. 

We do not advise to use public key pinning . Please contact us at [techinfo@datatrans.ch](mailto:techinfo@datatrans.ch) if you're currently using or plan to implement it.