# Exercise 02 - Backoffice Framework
## Expected Duration - 30 Minutes

For this exercise we are going explore the Backoffice Orchestration

#backoffice application works in a development mode, not in a production one
backoffice.cockpitng.additionalResourceLoader.enabled=true
backoffice.cockpitng.uifactory.cache.enabled=false
backoffice.cockpitng.widgetclassloader.resourcecache.enabled=false
backoffice.cockpitng.resourceloader.resourcecache.enabled=false
backoffice.cockpitng.development.mode=true



## Development configuration options


1. Open ``local.properties``
2. Add the following lines
```
backoffice.cockpitng.additionalResourceLoader.enabled=true
backoffice.cockpitng.uifactory.cache.enabled=false
backoffice.cockpitng.widgetclassloader.resourcecache.enabled=false
backoffice.cockpitng.resourceloader.resourcecache.enabled=false
backoffice.cockpitng.development.mode=true
```

3. Rebuild the application
4. Login into Backoffice
5. Navigate to breadbaord mode ``https://34.240.233.16:9002/backoffice/?mode=breadboard``
6. Explore the various Widgets
7. Revert back to standard backoffice
8. Press F4 and Edit Admin layout - close the West part of the page
9. Refresh page - to see changes (F4 to exist Orchestraion)
10. Reset both Widgets and UI
