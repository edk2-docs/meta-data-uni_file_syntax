## INF Module meta-data

If a Module’s INF file contains a MODULE_UNI_FILE entry in its [Defines] '
section, then the Unicode file specified may contain localization extensions 
for information found in the Module’s Abstract, Description, Copyright and 
Licenses part of the ```@file``` header in described in the "EDK II Module 
Information (INF) File Specification".

The following ```<Identifier>``` entries are reserved for extending the 
Module’s Abstract and Description content.

```pf
"STR_MODULE_ABSTRACT"
"STR_MODULE_DESCRIPTION"
```

If a Module’s INF file contains a Unicode file entry in its 
```[UserExtensions.TianoCore."ExtraFiles"]``` section, then that Unicode file 
may contain a localized version of a name for the module as well as other 
content. This file is used to hold content that is not required by UEFI PI 
Distribution Package, but may be useful for User Interface tools.

The following ```<Identifier>``` may be used to extend the name of the module.

```pf
"STR_PROPERTIES_MODULE_NAME"
```

Other content may be provided in this file as the file itself will be carried 
along with the Module in a UEFI PI Distribution Package.
