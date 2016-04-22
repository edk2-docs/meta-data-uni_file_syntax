## Package Meta-Data

If a Package’s DEC file contains a ```PACKAGE_UNI_FILE``` entry in its 
```[Defines]``` section, then the Unicode file specified may contain 
localization extensions for information found in the Module’s Abstract, 
Description, Copyright and Licenses part of the ```@file``` header in described 
in the "EDK II Package Declaration (DEC) File Specification". It may also 
contain content relevant to PCDs declared in the package.

The following ```<Identifier>``` entries are reserved for extending the 
Package’s Abstract and Description content.

```pf
"STR_PACKAGE_ABSTRACT"
"STR_PACKAGE_DESCRIPTION"
```

The following ```<Identifier>``` is reserved for extending the localization of 
a Token Space GUID’s error messages that are referenced by an error number. 
The C Name is the Token Space GUID’s C Name declared in the DEC file’s 
```[Guids]``` section.

```pf
"STR_" <CName> "_ERR_" <ErrorNumber>
```

The following ```<Identifier>``` entries are reserved for extending the 
localization of a PCD’s ```@HELP``` and ```@PROMPT``` content.

```pf
"STR_" <PcdName> "_HELP"
"STR_" <PcdName> "_PROMPT"
```

If a Package’s DEC file contains a Unicode file entry in its 
```[UserExtensions.TianoCore."ExtraFiles"]``` section, then that Unicode file 
may contain a localized version of a name for the package as well as other 
content. This file is used to hold content that is not required by UEFI PI 
Distribution Package, but may be useful for User Interface tools.

The following ```<Identifier>``` may be used to extend the name of the package.

```pf
"STR_PROPERTIES_PACKAGE_NAME"
```

Other content may be provided in this file as the file itself will be carried 
along with the Package in a UEFI PI Distribution Package.
