# Prototype Pattern

```
@startuml
'https://plantuml.com/class-diagram

interface Prototype {
    + clone()
}

class ConcretePrototype1 {
    + clone()
}

class ConcretePrototype2 {
    + clone()
}

class Client {
    # operation()
}

note left of Client::operation
    Object p = prototype.clone()
end note

note left of ConcretePrototype1::clone
    return copy of self
end note

note left of ConcretePrototype2::clone
    return copy of self
end note

Prototype <|.. ConcretePrototype1
Prototype <|.. ConcretePrototype2
Prototype <.up. Client: <<import>>

@enduml
```
