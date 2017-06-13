![](/assets/chain.png)

## Root Certificate Trust Store
We changed our certificate authority and therefore have a new chain of trust. Please check if you trust our new root certificates.  

## Certificate Pinning
If you pin our certificate, you should replace the existing certificate. Certificate pinning has some downsides, as the certificate rotation will occur on a regular basis in the future and you would need to update the certificates embedded within your application accordingly. Datatrans strongly advise **against **certificate pinning. 


## Public Key Pinning
If you extracted the public key from our certificate, please check our new public key with the embedded copy of your applications public key, as this public key has changed. If you use our Mobile Library you do **not** need to change anything.
