In order to support distributions conforming to the *UEFI PI Distribution 
Package Specification*, Unicode files may be used to contain localization 
content passed along in the XML file for content that cannot be passed using 
ASCII characters.

Literal strings (encapsulated by double quotation marks) in the following ENBF 
represent UCS-2 encoded character strings.

The format of the Unicode files that contain the optional Module and Package 
localization content for distribution is as follows:

```pf
<MetaUniFile> ::= <CommentLine>*
                  <MetaData>+

<MetaData>    ::= {<CommentLine>} {<BlankLine>} {<UnicodeLines>}
```

Additional Definitions used for Package Meta-Data ```<Identifier>``` entry of a 
```<Token>``` used in the Unicode file.

```pf
<ErrorNumber> ::= <HexDigitU>{1,8}

<PcdName>     ::= <CName> "_" <CName>

<CName>       ::= <Letter>({<Letter>} {<Digit>})*
```

Refer to Chapter 2.1, *Unicode Strings File Format* of the *Multi-String .UNI 
File Format Specification*, Extended Backus-Naur Form (EBNF) for the 
definitions of CommentLine, BlankLine and UnicodeLines.

It is also recommended that the comment section at the start of the files 
(described in the following sections of this chapter) use content consistent 
with content described for EDK II meta-data file headers, including a start tag 
line, ```// @file```, and include an abstract, description, copyright and 
license information.
