# .ini
## Intro
A file extension of configuration file.
## Syntax
### name-value pair

      The <name> will be set to <value>
      
       <name> = <value>

       where 
       
       <name> refers the variable name, it is a kind of indentifier <identifier> (defined below).

RE (Regular expression) 

We use RE to represent the syntax.

      <name> := <identifier>

      <value> := (<string>|<number>|<bool>)

where 

      <identifier> := <alpha>(<underscore>|<alpha>)*

      <string> := \"(<alpha>|<underscore>)+\"
      
      <number> := (<digit>)+

      <bool> := (True|False)
      
      <underscore> := _

      <alpha> := (<uppercase>|<lowercase>)

      <uppercase> := [A-Z]

      <lowercase> := [a-z]

      <digit> := [0-9]

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
        
## Principle
### Case-senstivity

"Section" is not equivalent to "section"

## Comments
### Single-line comment

The symbol refers the single-line comment.
      
      ;

Sometimes, it refers the single-line comment.

      #

Semicolons (;) at the beginning of the line indicate a comment. Comment lines are ignored.

## Escape character

The letter '\' is escaped character.

## Ref
https://en.wikipedia.org/wiki/INI_file

https://www.w3schools.io/file/ini-example-cheatsheet/

## Additional Reference
StackOverflow:

https://stackoverflow.com/questions/1378219/do-standard-windows-ini-files-allow-comments
##
