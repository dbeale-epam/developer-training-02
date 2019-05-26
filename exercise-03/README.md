# Exercise 02 - OCC Interactive Documentation
## Expected Duration - 15 Minutes

For this exercise we are going explore the interactive documenation of OCC

## Prerequsite
1. Ensure you have a working local copy of B2C Accelerator - which includes ycommercewebservices
2. Ensure you can navigate to `https://localhost:9002/rest/v2/swagger-ui.html`
3. Visit either electronics or apparel site and register a user

## Add OAuth2 Credentials

We need to create some OAuth2 client credentials

1. Got to Console; Impxex Import
2. Import the following client details ROLE_CLIENT:
```
INSERT_UPDATE OAuthClientDetails;clientId[unique=true]    ;resourceIds       ;scope        ;authorizedGrantTypes                                    ;authorities             ;clientSecret    ;registeredRedirectUri
                                ;client-side              ;hybris            ;basic        ;implicit,client_credentials                                     ;ROLE_CLIENT             ;secret          ;http://localhost:9001/authorizationserver/oauth2_implicit_callback;
                                ;mobile_android           ;hybris            ;basic        ;authorization_code,refresh_token,password,client_credentials    ;ROLE_CLIENT             ;secret          ;http://localhost:9001/authorizationserver/oauth2_callback;
```
3. Import the following client details ROLE_TRUSTED_CLIENT:
```
INSERT_UPDATE OAuthClientDetails;clientId[unique=true]    ;resourceIds       ;scope        ;authorizedGrantTypes                                            ;authorities             ;clientSecret    ;registeredRedirectUri 
                                ;trusted_client           ;hybris            ;extended     ;authorization_code,refresh_token,password,client_credentials    ;ROLE_TRUSTED_CLIENT     ;secret;         ;
```

## Explore the documentation

### anonymous calls
1. Try some calls that do not require authentication - Products 

### User calls
2. Try some calls that require a User parameter - e.g. Carts, enter registered user-id into call parameter and within Authorize section
```
clientid : mobile_android
secret : secret
```

### Trusted authentication cals
3. Try some calls that need extra authentication - Promotions - credential in flow : / applicatio 
```
clientid : trusted_client
secret : secret
```