# Postman Collection

# About

This collection allows developers to test APIs through [Postman](https://www.postman.com/) application.

# Prerequisites

* Postman desktop or web application
* Valid subscription to Schneider Electric API product
* User and data on Enedis or other utility providers

## Usage
 
* [Import collection](#import-collection)
* [Configure variables](#configure-variables)
* [Execute](#execute)


## Import collection

Import `EcoStruxure-Utility-Provider.postman_collection.json` to postman. Refer to [postman documentation to import a collection](https://learning.postman.com/docs/getting-started/importing-and-exporting-data/#importing-data-into-postman).

## Configure variables

Provision is provided at collection level to configure variables which are used across the postman requests.

![Postman Variables](/static/images/postman-variables.png)

| Variables|Comments|
|----------|--------|
|client_id|Client ID from API subscription. Go to Developer Portal for credentials.|
|client_secret|client secret from API subscription. Go to Developer Portal for credentials.|
|access_token|This will auto populated on execution of either `Exchange CIAM id_token` or `Impersonate an user` request|
|host|API server address, `se-exchange-uat-sandbox.apigee.net` for UAT sandbox, `api.exchange.se.com` for production|
 
## Execute

### Generate access token

Execute one of following to generate access token. On successful execution the access token will be automatically populated to collection variable for further API calls.

If you have access to CIAM ID token, use `Exchange CIAM id_token` request with id_token as body parameter to generate access token.

![Exchange CIAM id_token](/static/images/id-token-request.png)

If you do not have access to CIAM ID token, use `Impersonate an user` request with end customer email as body parameter to generate access token.

![Impersonate an user](/static/images/impersonate-token-request.png)

### Get consent from end user for Enedis meter access

To be completed.

### Get meters from Enedis

To be completed.

### Get daily consumption from Enedis

To be completed.
