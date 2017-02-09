---
-api-type: winrt method
---
 To import an issued certificate, it is not necessary for the certificate request to have been generated on the importing computer.
 The certificates included in the response need not be chained to trusted root certificates on the importing computer.
 The certificate is installed in the app container MY store.
 [Certification authority](http://msdn.microsoft.com/library/db46def4-bfdc-4801-a57d-d568e94a2dbb) and Root certificates are installed in the app container intermediate [certification authority](http://msdn.microsoft.com/library/db46def4-bfdc-4801-a57d-d568e94a2dbb) store.
 The key container name and key specification for the imported certificate are determined as described in the Remarks section of [PFXImportCertStore](http://msdn.microsoft.com/library/2c83774a-f2df-4d28-9abd-e39aa507ba88) with the exception that if AttributeId 1.3.6.1.4.1.311.17.1 is not present, MS_KEY_STORAGE_PROVIDER is always used as the provider name.