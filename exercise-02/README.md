# Exercise 02 - Backoffice Framework
## Expected Duration - 30 Minutes

For this exercise we are going explore the Backoffice Orchestration

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

1. Rebuild the application
2. Login into Backoffice
3. Navigate to breadbaord mode ``https://34.240.233.16:9002/backoffice/?mode=breadboard``
4. Explore the various Widgets
5. Revert back to standard backoffice
6. Press F4 and Edit Admin layout - close the West part of the page
7. Refresh page - to see changes (F4 to exist Orchestraion)
8. Reset both Widgets and UI

