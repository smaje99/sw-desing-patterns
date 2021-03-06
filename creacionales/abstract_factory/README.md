# Abstract Factory Pattern

```
@startuml
'https://plantuml.com/class-diagram

interface AbstractFactory {
    + createProductA()
    + createProductB()
}

class ConcreteFactory1
class ConcreteFactory2

interface AbstractProductA

class ProductA1
class ProductA2

interface AbstractProductB

class ProductB1
class ProductB2

class Client

AbstractFactory <|-up- ConcreteFactory1
AbstractFactory <|-up- ConcreteFactory2
AbstractProductA <|-- ProductA1
AbstractProductA <|-- ProductA2
AbstractProductB <|-- ProductB1
AbstractProductB <|-- ProductB2

AbstractFactory <.up. Client: <<import>>
AbstractProductA <.up. Client: <<import>>
AbstractProductB <.up. Client: <<import>>

ProductA1 <.. ConcreteFactory1: <<instance>>
ProductB1 <.. ConcreteFactory1: <<instance>>

ProductA2 <..ConcreteFactory2: <<instance>>
ProductB2 <..ConcreteFactory2: <<instance>>

@enduml
```
