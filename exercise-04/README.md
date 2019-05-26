# Exercise 02 - Backoffice Framework
## Expected Duration - 30 Minutes

For this exercise we are going create a new Backoffice extension and a widget
#backoffice application works in a development mode, not in a production one
backoffice.cockpitng.additionalResourceLoader.enabled=true
backoffice.cockpitng.uifactory.cache.enabled=false
backoffice.cockpitng.widgetclassloader.resourcecache.enabled=false
backoffice.cockpitng.resourceloader.resourcecache.enabled=false
backoffice.cockpitng.development.mode=true



## Create & Install the Backoffice extension

We now want to create a new extenstion

1. Run `ant extgen`, choose `ybackoffice` as template, name `mybackoffice`, package `org.officeco`
2. Say ``no`` to 
3. Browse the folders, you will notice a new extension called `mybacko` in the folder `custom`
4. We now have to add our new addon to `config/localextensions.xml`
5. Add the following block to the file

```xml
 <!-- Your new extension -->
 <extension name="myaddon"/>  
```


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