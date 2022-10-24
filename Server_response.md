```PlantUML
@startuml

participant "Authorisation Server" as RH << (S,#ADD1B2) Server >> order 3
participant "PI" as Alice #lightGreen
participant "Resource server" Bob #white

Alice -> Bob: Valid Authentication Request
Bob -> RH: formatted Authenticated Request (VALID)
RH --> Bob: Request Authenticated Response (OK)
Bob --> Alice: Authentication Response (OK)

Alice -> Bob: Invalid Authentication Request
Bob --> RH: formatted Authenticated Request (INVALID)
RH --> Bob: Request Authenticated Response (DENIED)
Alice <-- Bob: Authentication Response (DENIED)

@enduml
```
