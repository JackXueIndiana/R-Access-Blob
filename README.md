# R-Access-Blob
This article shows you how to access Azure Blob from R script using packages httr and RCurl to call Azure Blob REST API in order to create container, create bob and read blob.

We know that there is a Microsoft package called AzureSMR that provides ways to access Azur eblob and other service. BUt it requires the info on tenantID = "{TID}", clientID = "{CID}", authKey= "{KEY}, which are not always available for users. With CRAN packages httr and RCurl, we can access blob with account name and kay by making https calls to Blob REST API.

A good blog can be found at https://stackoverflow.com/questions/44519413/azure-put-blob-authentication-fails-in-r/, which we followed in this post.

To hide out the account name and access key, one may create a configuration file and put in a centralized place and in the R script a user can read the cfg file for the needed info.
