```PlantUML
@startuml
skinparam actorStyle awesome
actor Researcher as r
actor Lab Personnel as l
actor Bioinformatician as b
usecase "Submit Sample" as uc0
package Lab {
 usecase "Process Sample" as uc1
 usecase "Load Sample" as uc2
 usecase "Transfer data" as uc3
}
package Bioinformatics {
  usecase "Process data" as uc4
  usecase "Analysis" as uc5
  usecase "Deliver data" as uc6
}
r --> uc0
l --> uc1
l --> uc2
l --> uc3
b --> uc4
b --> uc5
b --> uc6
@enduml
```
