
# Description

Set of Policies helps you to integrate/connect the Axway API-Management solution with the external Identity-Provider: https://auth0.com.
The purpose is to provider Application-Developer the Self-Service capabilities they want using an API-Developer-Portal including API-Subscrioptions and on the other hand use a dedicated solution for Identity- & Token-Management.

![Self-Service-Flow](https://github.com/Axway-API-Management-Plus/auth0-apim-integration/blob/master/images/External_Token-Provider-Self-Service.png)



## API Management Version Compatibilty
This artefact can be used with Axway API Management version 7.6.2 and higher

## Prerequisites
An Auth0 Account - https://manage.auth0.com

## Configure Auth0
The API-Management solution will use the Auth0 Management REST-API to integrate. This API is secured using OAuth. 

Logon to your Auth0 Management console and make sure you have selected the correct tenant in the upper right corner. 
Now an application must be created, that corresponds to your API-Management solution and is used to access the Auth0 Management REST-API.
Steps needed:
 1. Applications sections
 2. Create application
 3. Name it e.g. Axway API-Management
 4. Type: Machine to Machine app.
 5. Create
 6. Select Auth0 Management API
 7. Authorize (here you may restrict permissions of this application)
 8. In the settings tab please note the Client ID & Secret for later

Later, when issuing access tokens, they will be issued only for a certain usage (audience) and this is named in Auth0 an API

 1. APIs section
 2. Create API
 3. Give it a friendly name: e.g. "My APIs", meaning, that these tokens can only be used to access APIs on your API-Management platform
 4. Provide the Identifier: e.g. https://api.customer-name.com - Will be used to validate the token at API-Management runtime.
 5. Leave the default Signing Algorithm

With that, we are done with the basic Auth0 setup. More advanced configuration is not in scope of this document. 

## Configure your API-Management solution


## API-Portal


## Changelog
- 0.0.4
  - Add HTTPS and MQTTS server support `--mqtts-*` `--https-*`
  - Add HTTPS client support for authz/authn with added cert verification  
  - Remove the 2 steps build: use docker 17.05 build capability

- 0.0.1 - 06.09.2018
  - Initial version


## Limitations/Caveats
- Nothing known

## Contributing

Please read [Contributing.md](https://github.com/Axway-API-Management-Plus/Common/blob/master/Contributing.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Team

![alt text][Axwaylogo] Axway Team

[Axwaylogo]: https://github.com/Axway-API-Management/Common/blob/master/img/AxwayLogoSmall.png  "Axway logo"


## License
[Apache License 2.0](/LICENSE)
