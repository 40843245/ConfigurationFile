# .ini
## Intro
A file extension of configuration file. 

A configuration file stores including:

Property of the setting.

It is loaded every time before the task starts to be executed.

For example,

Desktop.ini:

It stores the settings about Desktop, which is loaded every time after the computer or notebook etc finishes to be powered on.

The common use of it: 

Assign icon or thumbnail of folder.

## Syntax
### key-value pair

The <key> will be set to <value>. With the following syntax:
      
       <key> = <value>

or

      <key> : <value>
      
where 
       
       <key> refers the variable name, it is a kind of indentifier <identifier> (defined below).

RE (Regular expression) 

We use RE to represent the syntax.

      <key> := <identifier>

      <value> := <consideredAsString>

where 

      <identifier> := <alpha>(<underscore>|<alpha>)*
      
      <consideredAsString> := (<string_w>|<number_w>|<bool_w>)
      
      <string_w> := <string>(<whitespace><string)+
      
      <string> := ((\"(<alpha>|<underscore>)+\")
      
      <number> := (<digit>)+

      <bool> := (True|False)

      <whitespace> := ' '
      
      <underscore> := _

      <alpha> := (<uppercase>|<lowercase>)

      <uppercase> := [A-Z]

      <lowercase> := [a-z]

      <digit> := [0-9]

#### NOTICE 

NOTICE that

a number or a bool in <value> are considered as a string in .ini.

### section

     With [] annotation.

     Such as 
     
    [section]

### hierachy (section nesting)

    With dot in []. Dot is considered as delimiter. Sometimes, one can omit the first word.

    Such as 

    [section]
    domain = "example.com"
    
    [section.subsection]
    foo = bar

    Sometimes, it can be simplified as 

    [section]
    domain = "example.com"
    
    [.subsection]
    foo = bar
        
## General Principles
### Case-senstivity

Such as 

"Section" is not equivalent to "section"

### Comments
#### Single-line comment

The symbol refers the single-line comment.
      
      ;

Sometimes, it refers the single-line comment.

      #

NOTICE
      
      Comment lines are ignored.

      ; at the beginning of the line indicate a comment. 

      # is strongly not recommended.

### Escaped character

The letter slash '\' is an escaped character (to espace the letter that has special meaning).

The letter dollar sign '$' is also an escaped character. It is usually used to escape the character '$' or to represent a variable.

Such as 

      cost: $$80

## Ref
https://en.wikipedia.org/wiki/INI_file

https://www.w3schools.io/file/ini-example-cheatsheet/

## Additional Reference
StackOverflow:

It talks about comments.

https://stackoverflow.com/questions/1378219/do-standard-windows-ini-files-allow-comments

Python Official Docs:

It talks about the Python module -- configparser.

https://docs.python.org/3/library/configparser.html
