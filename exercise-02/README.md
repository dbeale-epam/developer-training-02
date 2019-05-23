# Exercise 02 - OCC Interactive Documentation
## Expected Duration - 15 Minutes

For this exercise we are going explore the interactive documenation of OCC

## Prerequsite
1. Ensure you have a working local copy of B2C Accelerator - which includes ycommercewebservices
2. Ensure you can navigate to `https://localhost:9002/rest/v2/swagger-ui.html`
3. Visit either electronics or apparel site and register a user

## Add 

We need to create some OAuth2 client credentials

1. Got to Console; Impxex Import
2. Import the following details:
```
INSERT_UPDATE OAuthClientDetails;clientId[unique=true]    ;resourceIds       ;scope        ;authorizedGrantTypes                                    ;authorities             ;clientSecret    ;registeredRedirectUri
                                ;client-side              ;hybris            ;basic        ;implicit,client_credentials                                     ;ROLE_CLIENT             ;secret          ;http://localhost:9001/authorizationserver/oauth2_implicit_callback;
                                ;mobile_android           ;hybris            ;basic        ;authorization_code,refresh_token,password,client_credentials    ;ROLE_CLIENT             ;secret          ;http://localhost:9001/authorizationserver/oauth2_callback;
```
3. 