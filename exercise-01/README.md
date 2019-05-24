# Exercise 01 - Addons
## Expected Duration - 30 Minutes

For this exercise we are going to modifing the standard B2C Commerce Storefront by creating and Addon and making modifcations here, leaving the Accelerator untouched

## Prerequsite
1. Ensure you have a working local copy of B2C Accelerator
2. Please refer to previous exercises for installation information

## Create & Install the Addon

We now want to create a new extenstion

1. Run `ant extgen`, choose `yaddon` as template, name `myaddon`, package `org.officeco`
2. Browse the folders, you will notice a new extension called `myaddon` in the folder `custom`
3. We now have to add our new addon to `config/localextensions.xml`
4. Add the following block to the file

```xml
 <!-- Your new extension -->
 <extension name="myaddon"/>  
```

Now need to install the Addon for the storefront

1. Now run `ant addoninstall -Daddonnames="MyAddon" -DaddonStorefront.yacceleratorstorefront="B2CStorefront"` 

## Now make some changes to  front-end components

1.  Note the *.txt files within the acceleratoraddon folder
2.  Modify contents of a file
3.  Build the system with `ant clean all`
4.  Note whole the files have been copied over to the target extension
