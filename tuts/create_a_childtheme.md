Create a new folder: user/themes/mytheme to house your new theme.
Create a new theme YAML file: /user/themes/mytheme/mytheme.yaml with the following content:
```
streams:
 schemes:
   theme:
     type: ReadOnlyStream
     prefixes:
       '':
         - user/themes/mytheme
         - user/themes/antimatter
 ```
 
 Change your default theme to use your new mytheme by editing the pages: theme: option in your user/config/system.yaml configuration file:
```
pages:
 theme: mytheme
 ```
