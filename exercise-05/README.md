# Exercise 05 - Custom OCC  Extension 
## Expected Duration - 15 Minutes

For this exercise we are going create a new OCC extension

## Create & Install the Backoffice extension

We now want to create a new extenstion

1. Run `ant extgen`, choose `ycommercewebservices` as template, name `mywebservices`, package `org.officeco`
2. Accept all default options 
3. Browse the folders, you will notice a new extension called `mywebservices` in the folder `custom`
4. We now have to add our new addon to `config/localextensions.xml`
5. Add the following block to the file

```xml
 <!-- Your new extension -->
 <extension name="mywebservices"/>  
```
6. Remove `ycommercewebservices` template from `localextensions.xml`
7. Run `ant clean all`
