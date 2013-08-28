# Visitor Pattern

Allows new operations to be added to existing object structures.

## Why is it useful

* Can create virtual functions to classes
* Functions use a Visitor interface, but implementation is unknown
* Handling of type is passed to the Concrete Visitor

## Why it isn't useful

* Its a little intrusive, you must implemenent the abstract "accept" method


## Implementation

    interface ElementVisitor {
        void visit(ElementA element);
        void visit(ElementB element);
    }
    
    interface Visitable{
        void accept(ElementVisitor visitor);
    }
    
    class ElementA implements Visitable{
        public void accept(ElementVisitor visitor){
            visitor.visit(this);
        }
    }
    
    class ElementB implements Visitable{
        public void accept(ElementVisitor visitor){
            visitor.visit(this);
        }
    }
    

## Participants

* Visitor Interface
* Concrete Visitor
* Element accepts Visitor

### Example Illustration <cite>[1]</cite>

![UML Diagram](http://upload.wikimedia.org/wikipedia/en/7/7f/VisitorClassDiagram.svg)

#References

1. [Wikipedia][]


[Wikipedia]: http://en.wikipedia.org/wiki/Visitor_pattern "Wikipedia"
