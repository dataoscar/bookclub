# Interpreter Pattern

Provides a mechanism to interpret sentences in a language using classes.

## Why is it useful?

* Problems and solutions may be expressed in a language
* Language can be sentenced like or specialized, lots of flexibility

## Implementation

    expression ::= plus | minus | variable | number  
    plus ::= expression expression '+'  
    minus ::= expression expression '-'  
    variable  ::= 'a' | 'b' | 'c' | ... | 'z'  
    digit = '0' | '1' | ... '9'  
    number ::= digit | digit number`   
> -- <cite>Wikipedia[1]</cite>

* Grammar rules defined as classes
* expression is the start symbol and literal is a terminal
* right hand side are instance variables
** plus, minus, variable, number

## Participants

* AbstractExpression   
Declares abstract interpret operation

* TerminalExpression  
    Implements terminal symbols such as numbers

* NonterminalExpression   
Implements expressions that are non-terminal, such as functions control structures.  
Typically recurses

### Example Illustration <cite>[1]</cite>

![Example UML Diagram](http://upload.wikimedia.org/wikipedia/en/0/03/Interpreter_UML_class_diagram.jpg)

#References

1. [Wikipedia][]


[Wikipedia]: http://en.wikipedia.org/wiki/Interpreter_pattern "Wikipedia"