@startuml
start
'!include plantuml-ae.iuml

participant "Request Handler" as RH  << (S,#ADD1B2) Server >> order 3

participant Alice #lightGreen
participant Bob #white

Alice -> Bob: Valid Authentication Request
Bob -> RH: formatted Authenticated Request (VALID)
RH --> Bob: Request Authenticated Response (OK)
Bob --> Alice: Authentication Response (OK)

Alice -> Bob: Invalid Authentication Request
Bob --> RH: formatted Authenticated Request (INVALID)
RH --> Bob: Request Authenticated Response (DENIED)
Alice <-- Bob: Authentication Response (DENIED)

'!include ../../plantuml-styles/ae-copyright-footer.txt
stop
@enduml
