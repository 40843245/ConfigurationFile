# .ini
## Intro
A file extension of configuration file.
## Syntax
### name-value pair

      The <name> will be set to <value>
      
       <name> = <value>

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
