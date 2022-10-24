```PlantUML
@startuml
protein.pdb -> protein.gro : pdb2gmx 
protein.gro -> solvated.gro : solvate
solvatd.gro -> salty.gro : genion
@enduml
```
