# Visitor Pattern

```
@startuml
'https://plantuml.com/class-diagram

class Client

interface Visitor {
    + visitConcreteElementA(concreteElementA)
    + visitConcreteElementB(concreteElementB)
}

class ConcreteVisitor1
class ConcreteVisitor2

interface Element {
    + accept(visitor)
}

class ConcreteElementA {
    + accept(visitor: Visitor)
    + operationA()
}

class ConcreteElementB {
    + accept(visitor: Visitor)
    + operationB()
}

note right of ConcreteElementA::accept
    visitor.visitConcreteElementA(this)
end note

note right of ConcreteElementB::accept
    visitor.visitConcreteElementB(this)
end note

Client -up-> Visitor
Client -right-> Element

Visitor <|.up. ConcreteVisitor1
Visitor <|.up. ConcreteVisitor2

Element <|.down. ConcreteElementA
Element <|.right. ConcreteElementB

@enduml
```
