# Strategy Pattern

```
@startuml
'https://plantuml.com/class-diagram

class Strategy {
    + algorithm()
}

class ConcreteStrategyA
class ConcreteStrategyB

class Context {
    + operation()
}

note left of Context::operation
    strategy.algorithm()
end note

Strategy <|.. ConcreteStrategyA
Strategy <|.. ConcreteStrategyB

Context "1" *-- "1" Strategy: - strategy

@enduml
```
