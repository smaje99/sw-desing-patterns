# Decorator

```
@startuml
'https://plantuml.com/class-diagram

interface Component {
    + operation()
}
class ConcreteComponent {
    operation()
}
abstract Decorator {
    + operation()
}
class ConcreteDecorator {
    + operation()
}

Component <|.. ConcreteComponent
Component <|.. Decorator
Decorator <|-- ConcreteDecorator

Decorator o-- Component: - component

@enduml
```
