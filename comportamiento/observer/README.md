# Observer Pattern

```
@startuml
'https://plantuml.com/class-diagram

interface Observer {
    + update()
}

interface Subject {
    + register(observer)
    + unregister(observer)
    + notifyAll()
}

class ConcreteObserverA
class ConcreteObserverB

note left of Subject::notifyAll
    for observer in observerCollection
        call observer.update()
end note

Observer <|.. ConcreteObserverA
Observer <|.. ConcreteObserverB

Subject o-- Observer

@enduml
```
