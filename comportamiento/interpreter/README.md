# Interpreter Pattern

````
@startuml
'https://plantuml.com/class-diagram

class Client
class Context
class AbstractExpression {
    + interpret(context: Context)
}
class TerminalExpression
class NonTerminalExpresion

AbstractExpression <|-- TerminalExpression
AbstractExpression <|-- NonTerminalExpresion
NonTerminalExpresion o--> AbstractExpression
Client --> Context
Client --> AbstractExpression

@enduml
```
