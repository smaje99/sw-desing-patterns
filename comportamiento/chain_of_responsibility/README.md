# Chain Of Responsibility

```
@startuml
'https://plantuml.com/class-diagram

interface Handler {
    + handleRequest()
}

class ConcreteHandler1
class ConcreteHandler2
class Client

Handler <|.. ConcreteHandler1
Handler <|.. ConcreteHandler2
Handler <-left- Client: "<<use>>"
Handler <-- Handler: "Next"

@enduml
```
